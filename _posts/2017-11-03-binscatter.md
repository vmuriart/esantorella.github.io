This post illustrates use of the Python module 
[binscatter](https://github.com/esantorella/binscatter, described at https://michaelstepner.com/binscatter/).
The [Stata package](https://michaelstepner.com/binscatter/) that inspired this module
has a far more extensive explanation of what a binned scatter plot is and how to
interpret it.

Let's say we want a visual representation of the relationship between wages and 
time spent on the job (tenure). People with more tenure have more job 
experience. We may want to understand how more tenure affects wages either 
with or without accounting for experience.

Let's start by making up some data. Note that if we were to regress wages on
experience and tenure, the coefficient on tenure would be 1, but if we regress
wages on tenure only, the coefficient is greater.

```python
import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
%matplotlib inline
import binscatter
```


```python
n_obs = 1000
data = pd.DataFrame({'experience': np.random.poisson(4, n_obs) + 1})
data['tenure'] = data['experience'] + np.random.normal(0, 1, n_obs)
data['wage'] = data['experience'] + data['tenure'] + np.random.normal(0, 1, n_obs)
data.head()
```



<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>experience</th>
      <th>tenure</th>
      <th>wage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8</td>
      <td>7.612358</td>
      <td>13.711054</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>3.721119</td>
      <td>7.987760</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4</td>
      <td>3.496378</td>
      <td>7.608632</td>
    </tr>
    <tr>
      <th>3</th>
      <td>9</td>
      <td>8.432021</td>
      <td>18.218504</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3</td>
      <td>2.439553</td>
      <td>4.583498</td>
    </tr>
  </tbody>
</table>
</div>




In the first plot, we'll break observations into twenty bins by their level of tenure. In the second figure, we'll residualize both wages and tenure using experience, so as to show the relationship of tenure and wages while holding experience constant. Normally, residuals have mean zero, but binscatter recenters the y variable to have its original mean.


```python
fig, axes = plt.subplots(2)
axes[0].binscatter(data, 'wage', 'tenure')
axes[0].legend()
axes[0].set_title('No controls')
axes[1].binscatter(data, 'wage', 'tenure', controls=['experience'])
axes[1].set_xlabel('Tenure (residualized)')
axes[1].set_ylabel('Wage (residualized, recentered)')
axes[1].legend()
axes[1].set_title('Controlling for experience')
plt.tight_layout()
plt.show()
```


![png]({{ site.url }}/binscatter_figs/output_4_1.png)


We can recenter x in the same way we recentered y. Doing this makes it visually clear that we are working with much less variation in x after accounting for z, and that the slope is much lower: tenure appears to matter less after accounting for experience.


```python
fig, axes = plt.subplots(2, sharex=True, sharey=True)
axes[0].binscatter(data, 'wage', 'tenure')
axes[0].legend()
axes[0].set_ylabel('Wage')
axes[0].set_ylabel('Tenure')
axes[0].set_title('No controls')
axes[1].binscatter(data, 'wage', 'tenure', controls=['experience'], recenter_x=True)
axes[1].set_xlabel('Tenure (residualized, recentered)')
axes[1].set_ylabel('Wage (residualized, recentered)')
axes[1].legend()
axes[1].set_title('Controlling for experience')
plt.tight_layout()
plt.show()
```



![png]({{ site.url }}/binscatter_figs/output_6_1.png)


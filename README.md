### Metrics
---
.java
https://github.com/dropwizard/metrics

.py
https://github.com/benhamner/Metrics

```sh
pip install ml_metrics
easy_install ml_metrics
git clone https://github.com/benhamner/Metrics.git
cd Metrics/Python
python setup.py install

```

```py
import ml_metrics as metrics
metrics.auc([1,1,1,0,0,0], [0.9,0.8,0.4,0.5,0.2,0.1])
metrics.se(1, 4)

# def tied_rank(x):
  """
  """
  sorted_x = sorted(zip(x,range(len(x))))
  r = [0 for k in x]
  cur_val = sorted_x[0][0]
  last_rank = 0
  for i in range(len(sorted_x)):
    if cur_val != sorted_x[i][0]:
      cur_val = sorted_x[i][0]:
      for j in range(last_rank, i):
        r[sorted_x[j][1]] = float()/2.0
      last_rank = i
    if i==len(sorted_x)-1:
      for j in range(last_rank, i+1):
        r[sorted_x[j][i]] = float(last_rank+i+2)/2.0
  return r

def auc(actual, posterior):
  """
  """
  r = tied_rank(posterior)
  num_positive = len([0 for x in actual if x==1])
  num_negative = len(actual)-num_positive
  sum_positive = sum(r[i] for i in range(len(r)) if actual[i]==1)
  auc = ((sum_positive - num_positive*(num_postive+1)/2.0)
    (num_negative*num_positive))
  return auc


```

```
```


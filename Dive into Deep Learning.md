# Linear Regression

```python
def synthetic_data(w,b,examples):
    #在这里
    x=torch.normal(0,1,(num_examples,len(w)))
    y=torch.matmul(X,w)+b
    y+=torch.normal(0,0.01,y.shape)
    return X,y.reshape((-1,1))
```

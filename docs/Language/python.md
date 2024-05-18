# Python

## Data type

### String

1. 格式化字符

```python
>>> name = 'Matt'
>>> print('Hello {}'.format(name))
Hello Matt


>>> print('I:{} R:{} S:{}'.format(1, 2.5, 'foo')) 
I:1 R:2.5 S:foo 
            
>>> 'Name: {}'.format('Paul') 
'Name: Paul' 
>>> 'Name: {name}'.format(name='John') 
'Name: John' 
>>> 'Name: {[name]}'.format({'name':'George'}) 
'Name: George'
 >>> 'Last: {2} First: {0}'.format('Paul', 'George','John') 
'Last: John First: Paul' 
```

2. 
## code 收集

### 窗宽窗位的处理

```python
def window(img, WL=50, WW=350):
    upper, lower = WL+WW//2, WL-WW//2
    X = np.clip(img.copy(), lower, upper)
    X = X - np.min(X)
    X = X / np.max(X)
    X = (X*255.0).astype('uint8')
    return X
```

相关代码博客:https://blog.csdn.net/oooortr?type=blog
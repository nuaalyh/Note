# Anaconda安装tensorflow遇到问题

##  problem

D:\Anaconda3\lib\site-packages\h5py\__init__.py:36: FutureWarning: Conversion of the second argument of issubdtype from `float` to `np.floating` is deprecated. In future, it will be treated as `np.float64 == np.dtype(float).type`.
  from ._conv import register_converters as _register_converters

## solution

According to [this link](https://stackoverflow.com/questions/48340392/futurewarning-conversion-of-the-second-argument-of-issubdtype-from-float-to)将numpy回退版本

For anyone coming here with *this* problem, it is a [known h5py issue](https://github.com/h5py/h5py/issues/974), introduced with [numpy 1.14](https://github.com/numpy/numpy/pull/9505). As stated by the devs:

> You can ignore the warning, it's not going to cause any issues at the moment, but you should upgrade to the next release of h5py when it becomes available.

... so it's harmless. The fix has just been [merged](https://github.com/h5py/h5py/pull/926) to master. But until the update is released, the workaround is to downgrade numpy to a previous version:

```
pip install numpy==1.13.0
```






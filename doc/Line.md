####    问题1
```bash
ModuleNotFoundError: No module named 'pytest'
```
缺少pytest包，于是在tf的环境下安装
```bash
conda activate tf
pip install bash
conda deactivate
```
`pytest安装在tf环境中安装成功`
![](2020-02-20-23-47-48.png)
####    问题2
![](2020-02-21-09-39-29.png)
于是我在Anaconda中安装了glog
![](2020-02-21-09-38-59.png)
但是该问题仍然出现。
推测为版本问题：
![](2020-02-21-09-44-25.png)
将其卸载
![](2020-02-21-09-42-04.png)
然后用pip安装
![](2020-02-21-09-43-33.png)
`安装完成`
![](2020-02-21-09-45-02.png)
`问题解决`
![](2020-02-21-09-45-50.png)
类似的问题，用pip安装了easydict、sklearn
####    问题3
`在pycharm终端中执行，找不到自定义模块`
![](![](2020-02-21-10-31-39.png).png)
肯定是环境变量的问题，先看一下现在的搜索路径
![](2020-02-21-10-35-09.png)
上图中的路径肯定是找不到自定义的额config模块的
[Ubuntu下Python导入自定义模块的三种方法](https://www.cnblogs.com/datou-swag/articles/10740132.html)
这里使用彻底修改，毕竟后面还要调试很多次，在.bashrc末尾加入了
```bash
export PYTHONPATH="/home/gong/Git/TensorFlow/lanenet-lane-detection:$PYTHONPATH"
```
![](2020-02-21-10-53-41.png)
`pycharm终端输出`
![](2020-02-21-10-59-53.png)
该问题解决
####    问题4
`找不到模型`
![](![](2020-02-21-11-13-26.png).png)
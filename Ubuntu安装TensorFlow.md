# Ubuntu 16.04 安装 TensorFlow
### 1.查看python版本
#### 打开终端，输入指令
```
python
```
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/1.PNG)

#### 可以看到，默认安装的python版本是2.7

### 2.安装pip和依赖包

#### （1）输入指令

```
sudo apt-get install python-pip python-dev 
```
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/2.PNG)
#### （2）root模式会让输入密码，密码是隐藏的，输入后，直接回车，安装就会往下进行
#### （3）在显示 Do you want to continue？ 时，输入y，并回车
### 3.升级 pip 及 apt-get
#### （1）升级pip，输入指令
```
sudo pip install --upgrade pip
```
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/3.PNG)
#### （2）升级apt-get，输入指令
```
sudo apt-get update
```
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/4.PNG)
 
### 4.安装Tensorflow
#### 输入指令 
```
sudo pip install tensorflow
```
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/5.PNG)
#### 同样需要输入一次密码，在显示：
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/6.PNG)
#### 表示安装完成了~

### 5.测试Tensorflow是否安装成功
#### （1）打开终端，输入指令
```
python
```
#### （2）输入以下指令，进行测试
```python
import tensorflow as tf
a=tf.constant([1.0,2.0,3.0],shape=[3],name='a')
b=tf.constant([1.0,2.0,3.0],shape=[3],name='b')
c=a+b
sess=tf.Session(config=tf.ConfigProto(log_device_placement=True))
print sess.run(c)
```
运行结果为：
 ![image](https://github.com/lucia-ly/test2/blob/master/pic1/7.PNG)

恭喜~安装成功喽！

#### P.S.
在安装TensorFlow时，很可能会遇到报错，有说是网络问题的，也有别的说法，究竟是什么问题导致的，现在还没办法给出确切的答案（大概是玄学吧），如果遇到这种问题，那就多装几次~

把pip和apt-get都更新了，亲测是解决报错行之有效的方法，笔者水平有限，如果有问题，欢迎指正~

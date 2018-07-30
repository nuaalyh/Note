### Linux  增加用户sudo权限

参考：[为用户增加sudo权限(修改sudoers文件)](https://blog.csdn.net/younger_china/article/details/23349249)

1. 输入：su root ，输入密码进入root权限

2. 查看etc/sudoers文件权限，如果是只读，改为可写

   ls -l /etc/sudoers  

   修改可写：chmod 777 /etc/sudoers 

   再重新输入ls -l /etc/sudoers查看文件权限，已改为读写

3. 输入：visudo，回车

   找到#User privilege specification一行，在下面root  ALL=(ALL)  ALL下面输入username ALL=(ALL) ALL，齐其中username是你要添加sudo权限的用户名

4. Ctrl+ O保存，回车，Ctrl+X退出

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   
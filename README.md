# Beyond Compare 4.2.10注册机

#### 介绍（如果对你有用，请给个star！）
master分支支持破解Beyond Compare 4.2.10(当前最新版)和Beyond Compare 4.2.9, 但破解速度比较慢,
crack4.2.9分支只支持破解Beyond Compare 4.2.9，但破解速度快，使用方法：把BCompareCrack.exe拷贝到Beyond Compare安装目录，点击运行就可以

以下Beyond Compare 4.2.9反汇编分析：

call bcompare.BFB730是计算exe是否被修改过和是否超出试用期限
![输入图片说明](https://images.gitee.com/uploads/images/2019/0804/010609_a608f578_1650820.png "权限判断函数.png")

经过第一个call后，在执行到call bcompare.853E00前，在地址ecx+0x600储存权限校验结果数据，后面很多判断都是基于这里的校验结果(bcompare.853E00直接赋值给eax就是用作后面的判断，应该弹出哪个提示框以及是否可以继续使用)
这里我们直接改写bcompare.853E00，给ecx+0x600赋值0x500(为什么是0x500?, 因为经过多次比较值为0x500可以使用软件，0x0E02不可使用)
![输入图片说明](https://images.gitee.com/uploads/images/2019/0807/110921_5d62b09d_1650820.png "QQ图片20190807110600.png")

要修改的代码对应文件偏移如下(下面没有去掉提示框，要去掉提示框可以查看代码)，
![输入图片说明](https://images.gitee.com/uploads/images/2019/0804/010641_06c07a05_1650820.png "exe文件修改位置.png")

#### 软件架构
软件架构说明


#### 安装教程

不需要安装，只需把BCompareCrack.exe拷贝到Beyond Compare安装目录，点击运行就可以

#### 使用说明

将\Release\BCompareCrack.exe拷贝到Beyond Compare 4目录下然后运行即可，也可以自已编译

#### 参与贡献

1. Fork 本仓库
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request


#### 码云特技

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2. 码云官方博客 [blog.gitee.com](https://blog.gitee.com)
3. 你可以 [https://gitee.com/explore](https://gitee.com/explore) 这个地址来了解码云上的优秀开源项目
4. [GVP](https://gitee.com/gvp) 全称是码云最有价值开源项目，是码云综合评定出的优秀开源项目
5. 码云官方提供的使用手册 [https://gitee.com/help](https://gitee.com/help)
6. 码云封面人物是一档用来展示码云会员风采的栏目 [https://gitee.com/gitee-stars/](https://gitee.com/gitee-stars/)
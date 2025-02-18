# Course note
This is my , especially for math course.
https://mhqqysh.cn
My name is Shihong Yuan, a 2023 ZJUer & UIUCer My personal github is https://github.com/mhqqysh
# Menu

目标
1. cmu10-414 
    1. 课程🐕  0/23
    2. assignment🐕 0/5
2. cs149
    1. 课程       0/18
    2. assignment     0/4


I want to commit this one everyday but the difficulties are
1. how to add pictures easitly
2. how to submit here but also change in the other




现在急需搞定的事情
1. cuda怎么学
2. 这两个课程怎么学起来，代码怎么快跑起来



## 其他问题
1. 改完文件其实就可以网站响应，就是不需要本地hugo server 因为github workflow里面有这个过程
2. 现在vscode连接github唯一的问题就是有时候连不上网络，感觉就是本地克隆一个验证一下已经可以连接上了



<!--
git clone下来问题
0. git kraken 设置-》integrations->github->生成新的，然后连接【已经不用】
1. 需要先把theme里面的文件删掉，然后在git submodule update
2. 不能有两个readme.md -->


# 现在步骤
1. 改文件 
2. vscode里面提交+同步
3. 如果要拉取就是点git里面循环的标志就行

更新步骤
1. 打开文件夹,终端
2. hugo new --kind post post/1.md 
3. hugo server然后本地看着修改
4. vscode里面保存（包括了view change等等）  提交
5. https://zhuanlan.zhihu.com/p/624521466 然后本地克隆一个验证一下已经可以连接上了，之后就可以随意vscode pull了，不需要gitkraken了


突然发现

1. ssh或者gitkraken加入连接 其实都不用了

因为我现在本地就是绑定的大号mhqqysh，所以不需要再连接别的了
如果要连接别的话，就需要vscode更新成新的号的
其实vscode连接账号也就相当于gitkraken连接账号，哎，真是，简单的

但是搞清楚了一点，就是直接把我现在的isa给别人就可以连接了，不需要新建一个，即使是两个账号

还有一个问题怎么选择的不同账号，，是不同的isa_。pub吗。作为连接服务器和连接远程仓库的不同

2. 不需要pull request如果有了权限的话


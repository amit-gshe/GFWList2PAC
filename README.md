GFWList2PAC
===========
### 将GFWList条目转换成PAC文件：

    
    进入项目主页后，右上角选择，Clone or Download，选择Download Zip。
    
    下载后，解压项目。进入目录，找到main.py文件，打开。
    
    找到变量gfwlist_url，修改为https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt，保存退出。
    
    确认计算机安装好Python2环境后，命令后进入该文件夹，执行命令：
    
    main.py -f 输出代理文件路径/生成文件.pac -p “代理参数” 例如：``` main.py -f d:/gfw.pac -p “SOCKS5 127.0.0.1:1080;”```
    
    
### Usage

    usage: main.py [-h] [-i GFWLIST] -f PAC -p PROXY [--user-rule USER_RULE]

    optional arguments:
      -h, --help            show this help message and exit
      -i GFWLIST, --input GFWLIST
                            path to gfwlist
      -f PAC, --file PAC    path to output pac
      -p PROXY, --proxy PROXY
                            the proxy parameter in the pac file, for example,
                            "SOCKS5 127.0.0.1:1080;"
      --user-rule USER_RULE
                            user rule file, which will be appended to gfwlist

### Example

    main.py -i gfwlist.txt -f proxy.pac -p "PROXY 127.0.0.1:8087"

    you can download gfwlist.txt yourself

    you can add a custom list into gfwlist2pac/resources/custom.txt

    and add a ban list which you want a direct connection into gfwlist2pac\resources\ban.txt


fork from [clowwindy](https://github.com/clowwindy/gfwlist2pac)

```
contect mmgac001[at]gmail.com or comit issues if you have any idea
```


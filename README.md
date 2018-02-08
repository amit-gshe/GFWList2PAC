GFWList2PAC
===========
进入项目主页后，右上角选择，Clone or Download，选择Download Zip。
下载后，解压项目。进入目录，找到main.py文件，打开。
找到变量gfwlist_url，修改为https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt，保存退出。
确认计算机安装好Python环境后，命令后进入该文件夹，执行命令：
main.py -f 输出代理文件路径/生成文件.pac -p “代理参数” 例如： main.py -f ~/gfw.pac -p “SOCKS5 127.0.0.1:1080;”
参数需要自行调整，工具支持自定义规则，请各位参考项目文档。工具执行后，会在您指定的位置产生PAC文件。
运行ShadowSocks，本文章以macOS系统为例。点击小飞机图标，选择“编辑自动模式的PAC”，然后系统会弹出窗口，并自行选中gfwlist.js。
编辑该文档，将生成的PAC文件内容，替换gfwlist.js文档内容，保存并退出。
重新运行ShadowSocks，开启代理即可
Generate O(1) PAC file from gfwlist.

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


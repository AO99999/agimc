# agimc
Accelerate github in mainland China

在中国大陆加速Github

1. GitHub 镜像

常用镜像地址：

https://github.com.cnpmjs.org

https://hub.fastgit.org

Github镜像简单理解为Github网站的完整、同步克隆，具备Github网站相同功能.

2. GitHub 文件加速

利用 Cloudflare Workers 对 github release 、archive 以及项目文件进行加速，部署无需服务器且自带CDN.

https://gh.api.99988866.xyz

https://g.ioiox.com

参考开源项目：gh-proxy-GitHub(https://hunsh.net/archives/23/) 

3. Github 加速下载工具

http://toolwa.com/github/
复制当前 GitHub 地址粘贴到输入框中加速下载

https://github.zhlh6.cn
输入 Github 仓库地址，使用生成的地址进行 git ssh 等操作

4. GitHub raw 加速

GitHub raw 域名并非 github.com 而是 raw.githubusercontent.com，“方法4”中GitHub加速工具如不能加速此域名，可使用 Static CDN 反代服务。

将 raw.githubusercontent.com 替换为 raw.staticdn.net 即可加速。

5. GitHub + Jsdelivr

jsdelivr 不能获取 exe 文件以及 Release 处附加的 exe 和 dmg 文件

即如 exe 文件是附加在 Release 处但未在 code 中时，无法获取。只能当作静态文件 cdn 用途，而不能作为 Release 加速下载的用途。

6. 通过 Gitee 中转 fork 仓库下载

登录https://gitee.com/，选择“从 GitHub/GitLab 导入仓库”

在导入页面中粘贴Github仓库地址，点击导入，

导入操作完成后，可在导入的仓库操作 GitHub 仓库代码，可点击仓库顶部“刷新”按钮同步 Github 代码仓库.

7. 修改 HOSTS 文件

访问IP查询网址获取以下地址对应IP：
github.com
github.global.ssl.fastly.net
assets-cdn.github.com

IP查询网址：
https://www.ipaddress.com/
http://tool.chinaz.com/（大陆地区推荐）


Hosts文件路径：
Windows操作系统：   
C:\Windows\System32\drivers\etc\hosts

linux操作系统：
/etc/hosts

（注：1、Windows系统修改C:\Windows\System32\drivers\etc\hosts文件的权限，
指定可写入：右击->hosts->属性->安全->编辑->点击Users->在Users的权限“写入”后面打勾后确定.
2、右击->hosts->打开方式->选定记事本（或其他编辑器）->在末尾处添加如下内容（例，以实际为准）：

# #Github
13.250.177.223   github.com

162.125.32.5  github.global.ssl.fastly.net

185.199.109.153  assets-cdn.github.com


CMD或Powershell输入 ipconfig /flushdns
刷新DNS解析缓存.

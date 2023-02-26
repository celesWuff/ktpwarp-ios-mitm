# ktpwarp-ios-mitm

ktpWarp：课堂派自动签到 - iOS MITM 模块

将这里的模块安装到您 iPhone 或 iPad 上的 Shadowrocket/Quantumult X/Surge/Loon/Stash/Egern 中，您就可以使用包括微信在内的任何扫码工具，将课堂派的签到二维码提交给您的 ktpwarp-server，从而摆脱课堂派无比缓慢的加载速度，实现更快速的签到。

如果您想要使用这里的模块，您需要一台运行 ktpwarp-server 的服务器。

了解 ktpwarp-server: https://github.com/celesWuff/ktpwarp-server

## 注意

ktpWarp 仍处于 Beta 阶段，这代表 ktpWarp 尚未在生产环境中得到大规模的验证。

因此，ktpWarp 仍可能存在着未知的 Bug 或签到“脱靶”。如果您发现了 Bug，欢迎您在 Issues 中报告。

## 它怎么工作呢？

在这些网络工具 app 的帮助下，当您在您的 iOS 设备上扫描并访问课堂派签到二维码时，我们能够通过 MITM（中间人攻击）的方式，自动地解密网络请求，获取二维码签到的参数，并将这些参数转交给 ktpWarp 的网页客户端。

## 安装

**注意：我们建议您配置完成后，立刻使用您将会使用的扫码工具，扫描一张过期或不存在的二维码，然后连接上您的服务器。这样，当您下一次扫码时，您就可以立刻看到签到结果，而不再需要反复重新输入服务器地址了。**

### Shadowrocket

[点击安装](shadowrocket://install?https://raw.githubusercontent.com/celesWuff/ktpwarp-ios-mitm/master/ktpwarp-surge.sgmodule)

### Quantumult X

[点击安装](quantumult-x:///add-resource?remote-resource=%7B%22rewrite_remote%22%3A%5B%22https%3A%2F%2Fraw.githubusercontent.com%2FcelesWuff%2Fktpwarp-ios-mitm%2Fmaster%2Fktpwarp-quantumultx.conf%2Ctag%3Dktpwarp%22%5D%7D)

### Surge

安装路径：首页 > 模块 > 安装新模块

https://raw.githubusercontent.com/celesWuff/ktpwarp-ios-mitm/master/ktpwarp-surge.sgmodule

### Loon

[点击安装](loon://import?plugin=https://raw.githubusercontent.com/celesWuff/ktpwarp-ios-mitm/master/ktpwarp-loon.plugin)

### Stash

安装路径：首页 > 覆写 > 安装覆写

https://raw.githubusercontent.com/celesWuff/ktpwarp-ios-mitm/master/ktpwarp-stash.stoverride

### Egern

安装路径：首页 > 工具 > 模块

https://raw.githubusercontent.com/celesWuff/ktpwarp-ios-mitm/master/ktpwarp-egern.yaml

---

如果您没有配置过 MITM，或者如果您完全不知道这是什么，那么您需要按如下步骤配置 MITM：

### Shadowrocket

Shadowrocket > 配置 > 正在使用的配置文件右侧的“i” > HTTPS 解密 > 生成新的 CA 证书 > 安装证书

系统设置 > “已下载描述文件” > 安装

系统设置 > 通用 > 关于本机 > 证书信任设置 > 勾选刚刚下载的证书

回到 Shadowrocket 的“HTTPS 解密”页面，确认“HTTPS 解密”已经打开。

### Quantumult X

Quantumult X > 风车 > MitM > 生成证书 > 配置证书

系统设置 > “已下载描述文件” > 安装

系统设置 > 通用 > 关于本机 > 证书信任设置 > 勾选刚刚下载的证书

回到 Quantumult X，确认“重写”和“MitM”已经打开。

### Surge

Surge > MitM > 配置根证书 > 生成新的 CA 证书 > 安装证书

系统设置 > “已下载描述文件” > 安装

系统设置 > 通用 > 关于本机 > 证书信任设置 > 勾选刚刚下载的证书

回到 Surge，确认刚刚安装的模块、“Rewrite”和“MitM”已经打开。

### Loon

Loon > 配置 > MitM > 生成新的证书 > 安装证书

系统设置 > “已下载描述文件” > 安装

系统设置 > 通用 > 关于本机 > 证书信任设置 > 勾选刚刚下载的证书

回到 Loon，确认刚刚安装的插件、“复写”和“MitM”已经打开。

### Stash

Stash > MitM > CA 证书 > 生成新的 CA 证书 > 安装证书

系统设置 > “已下载描述文件” > 安装

系统设置 > 通用 > 关于本机 > 证书信任设置 > 勾选刚刚下载的证书

回到 Stash，确认刚刚安装的覆写和“MitM”已经打开。

### Egern

Egern > 工具 > MITM > 证书 > 生成新证书 > 安装证书

系统设置 > “已下载描述文件” > 安装

系统设置 > 通用 > 关于本机 > 证书信任设置 > 勾选刚刚下载的证书

回到 Egern，确认刚刚安装的模块和“MITM”已经打开。

## 许可证

MIT License

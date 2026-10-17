# 凌云志 发布仓

这个仓库只放「凌云志」阅读器的发布包，不放源码。

程序里的更新检查读的是本仓的 latest release：
    https://api.github.com/repos/ciquyuheshi/lingyunzhi/releases/latest

每次发版的资产有两个：
- Reader-v<版本>-windows-x64-portable.zip —— 便携版自动更新用（程序自己下载它）
- 凌云志-v<版本>.zip                    —— 整包，新机器安装用

仓库必须保持**公开**：程序下载更新包走 github.com 域名，私有仓的资产要带令牌，
而令牌不能塞进发给别人的软件里。

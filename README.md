# 凌云志 发布仓

**这个仓库不含源码。** git 里只有本文件；代码只以编译后的 `Reader.exe`
（Rust 后端 + 已内嵌的网页前端）与必须随包运行的中转脚本形式发布。

程序里的更新检查读的是本仓的 latest release：
    https://api.github.com/repos/ciquyuheshi/lingyunzhi/releases/latest

每次发版的资产有两个：
- `Reader-v<版本>-windows-x64-portable.zip` —— 便携版自动更新用，程序自己下载它
- `LingYunZhi-v<版本>.zip` —— 整包，新机器安装用

## 为什么资产名是英文

实测 GitHub 的上传接口会把中文名里的汉字整段丢掉
（`凌云志-v1.5.6.zip` 会落成 `-v1.5.6.zip`，字节数正确、名字错误），
所以资产名一律用 ASCII，发版脚本里有一道硬闸拦非 ASCII 名。

## 为什么仓库必须公开

程序下载更新包走 `github.com` 域名。私有仓的资产地址需要带令牌，
而令牌不能塞进发给别人的软件里——所以这个仓必须保持公开。
公开的只是发布包，不是源码。

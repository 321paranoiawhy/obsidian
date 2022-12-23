# 安装

## `Windows`

[NVM for Windows - GitHub](https://github.com/coreybutler/nvm-windows)
[NVM for Windows - Releases](https://github.com/coreybutler/nvm-windows/releases)
[卡斯伯's Blog](https://www.casper.tw/development/2022/01/10/install-nvm/)

## `MacOS`

[# Node Version Manager - GitHub](https://github.com/nvm-sh/nvm)

# 配置环境变量

## `Windows`

# 常用命令

```bash
# 查看当前 nvm 版本
nvm -v # nvm --version
# 1.1.10

# 安装指定的 node 版本
nvm install 14.15.5 # nvm i 14.15.5

# 列出已安装的 node 版本
nvm list # nvm ls
#   * 16.18.0 (Currently using 64-bit executable)
#     14.15.5

# 列出所有可用的 node 版本
nvm list avaiable # nvm ls avaiable

# 列出远端可用的 node 版本
nvm list-remote # nvm ls-remote

# 使用 14.15.5 版本的 node
nvm use 14.15.5 # Now using node v14.15.5 (64-bit)

node -v # node --version
# v14.15.5
```
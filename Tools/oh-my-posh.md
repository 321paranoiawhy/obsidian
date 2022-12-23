# 安装 `oh-my-posh`

[Installation - windows - winget](https://ohmyposh.dev/docs/installation/windows#installation)

```bash
winget install JanDeDobbeleer.OhMyPosh -s winget
```

# 确定当前 `shell` 类型

```bash
oh-my-posh get shell # powershell
```

# 打开 `Powershell` 配置文件

```bash
code $PROFILE # 使用 VS Code 打开配置文件
notepad $PROFILE # 使用记事本(notepad) 打开配置文件
```

如果未找到该配置文件, 可通过以下命令创建一个新的配置文件:

```bash
New-Item -Path $PROFILE -Type File -Force
```

# 插件下载

# `PSReadLine`

[PSReadLine - GitHub](https://github.com/PowerShell/PSReadLine#install-from-powershellgallery-preferred)

```
Install-Module -Name PowerShellGet -Force
```

查看已有历史输入命令: 

[### History Cmdlets - Powershell](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_history?view=powershell-7.3#history-cmdlets)

```bash
Get-History
history # 或输入 alisa: 首字母 h
```

# 配置

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Import-Module -Name Terminal-Icons
oh-my-posh init pwsh --config '$env:POSH_THEMES_PATH\jandedobbeleer.omp.json' | Invoke-Expression
```

# 列出所有主题

```bash
Get-PoshThemes
```

文件路径(供参考): `C:\Users\Administrator\AppData\Local\Programs\oh-my-posh\themes`

用户环境变量: `POSH_THEMES_PATH`
变量值: `C:\Users\Administrator\AppData\Local\Programs\oh-my-posh\themes`

# 查看帮助命令

```bash
help posh
```

# 查看 `Powershell` 安装路径

```bash
$psHome # C:\Windows\System32\WindowsPowerShell\v1.0
```

# 查看 `Powershell` 版本

```bash
$PSVersionTable.PSVersion
```

# 去除 `Powershell` 顶部广告

```json
# 已过时
"terminal.integrated.shellArgs.windows": ["-NoLogo"]

# 改用下面的配置
"terminal.integrated.profiles.windows": {
	"PowerShell": {
		"source": "PowerShell",
		"icon": "terminal-powershell",
		"args": ["-NoLogo"]
},
},
"terminal.integrated.defaultProfile.windows": "PowerShell",
```
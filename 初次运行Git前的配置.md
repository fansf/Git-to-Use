# 初次运行Git前的配置
[TOC]
## 配置文件
Git有三个配置文件：
> - /etc/gitconfig 全局，每个用户及他们仓库的通用配置        传递 `--system` 使之生效
> - ~/.gitconfig 或 ~/.config/git/config 当前用户的配置        传递`--global` 使之生效
> - .git/config  当前使用仓库的Git目录中的config文件

（如果有linux的知识，上面应该好懂）
## 用户信息
安装完git的第一件事就是配置你的用户名和邮件地址。每一个Git的提交都会使用这些信息，并且它会写入到你的每一次提交中，不可更改：
```bash
git config --global user.name "your name"
git config --global user.email your_email_address
```

`--global`会对你的所有仓库应用同一信息，当你想对不同的仓库使用不同的信息时，请使用不带`--global`的命令

很多GUI工具会在第一次运行时帮助你配置这些信息

## 文本编辑器
git默认的文本编辑器是vim，如果不知道vim的话，可能会有一些麻烦

## 检查配置信息
```bash
git config --list
```
或者
```bash
git config <key>
```

## 获取帮助
```bash
git help <verb>
git <verb> --help
man git-<verb>
```

如：
```bash
git help config
```
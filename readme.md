# goctl

English | [简体中文](readme-cn.md)

Read document at https://go-zero.dev/docs/goctl/goctl

## sxwl魔改
因为sxwl使用monorepo风格管理代码仓库，go微服务的main入口和etc在`/cmd/<service>/`目录下，其他代码在`/internal/<service>/`下。这和gozero生成的目录结构是不兼容的。

这里魔改一下goctl的代码以适应。

## 安装
在项目根目录执行
```bash
go install
```

## 验证
```bash
goctl -v
```
如下输出，代表安装成功

```text
goctl version 1.6.2-sxwl darwin/arm64
```
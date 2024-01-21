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

## 使用
与原始goctl使用一样，go子命令增加了一个--service参数，微服务的名字。

示例：3k项目下scheduler服务的api文件更新后，如何重新生成go代码，

```bash
cd /path/to/the/project/3k

goctl api go --style go_zero \
  --home ./tools/go-zero-template \
  --dir . \
  --api ./cmd/scheduler/scheduler.api \
  --service scheduler
```

# monorepos


## 目录结构

```html
root-repos/
  |-- applications/ "子仓库（项目级别）"放这里
  |     |-- my-next-app/
  |     |-- my-react-app/
  |-- node_modules/
  |-- packages/ "子仓库（共享库级别）"放这里
  |     |-- money/
  |     |-- queue/
  |-- .editorconfig
  |-- .gitignore
  |-- .yarnrc.yml
  |-- package.json
  |-- README.md
  |-- yarn.lock
```

## 常见问题

1. 在哪里安装公共依赖？
2. 公共依赖版本不一致怎么办？
3. 仓库中package-A怎么引用同级的package-B
4. package-B存在bug，package-A怎么办？
5. package-B破坏性修改，package-A怎么办？
6. 哪些代码可以定义为单独的 package？

## 原则

1. 只需要在仓库根目录执行命令
2. 每个`package`都是独立的
   1. 拥有自己的指令（开发、测试、启动）
   2. 功能完整，可以独立发布
3. 不需要关注
   1. 多个`package`存在相同依赖包，版本一致
   2. 多个`package`存在相同依赖包，但版本不一致
   3. 仓库中的`package`相互（循环）依赖

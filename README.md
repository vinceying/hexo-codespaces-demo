# hexo-codespaces-demo

前端在线编辑博客，使用 Codespace 搭建 Hexo 博客

## Fork 使用

#### 1.Fork 本仓库

如果想要快速开始可以 Fork 本仓库，建立 Codespaces 环境。

#### 2.修改部署参数（使用代码托管平台部署）

仓库主要有 `blog` 和 `static`，两个文件夹，`blog` 用于存放 hexo 文件，`static`用于存放静态资源。

部署参数（如果需要部署在代码托管平台，请修改此参数），默认分支为 `gh-pages`。

```shell
hexo config deploy.repository git@github.com:[yourgitname]/[repository name].git
```

#### 3.设置主题及配置主题参数

修改 Hexo 配置项和主题配置项，完善配置项后即可进入下一部。

#### 4.预览和部署

输入 `hexo s` 后 Codespaces 会将 Local Address 映射到公网，可进行预览。

##### 使用 hexo deploy 部署

确保第二步修改完参数后，进行 hexo 三连。

```
hexo clean
hexo g
hexo d
```

##### 使用 Vercel 或 Netlify 等 JAMStack 平台部署

使用此类平台部署选择对应仓库即可，但是由于 Hexo 源文件没有在根目录，注意填写 `ROOT DIRECTORY` 项，比如这里填写 blog。

##### 其它部署

关于部署到服务器和 OSS 等平台，可以通过 GitHub Action 来实现，请查阅相关文档。
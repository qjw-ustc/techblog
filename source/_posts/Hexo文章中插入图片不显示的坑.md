---
title: Hexo文章中插入图片不显示的坑
top: false
cover: false
toc: true
mathjax: false
date: 2021-11-30 22:04:48
password:
summary:
tags: [Hexo]
categories: [博客搭建]
---

### 问题描述

可能很多小伙伴在尝试搭建Hexo博客并发表文章时遇到一个问题, 那就是在文章中插入外部图片时无法正确显示, 我也遇到了同样的问题并且折腾了很久, 所以在这里记录下最终解决的方法

### 环境及版本

- 操作系统: Ubuntu 18.04 LTS (Windows同样验证可行)
- Hexo版本:  
  - hexo: 5.4.0
  - hexo-cli: 4.3.0
- 主题: Matery

_**一定要注意! 参考本文时要注意自己的版本是否一致, 否则可能需要参考其他博主的方法, 很重要!**_

### 解决办法

1. 修改博客根目录的```_config.yml```配置文件, 将```post_asset_folder```改为```true```

```yaml
post_asset_folder: true
```

2. 此时执行新建文章命令时, 会自动创建文章同名的目录, 例如:

```shell
hexo new post my-new-post
```

则会在```source/_posts/```目录下同时出现```my-new-post.md```文件和明文```my-new-post```的目录(中文也可以, 亲测).

3. 在该目录中放入需要显示的图片, 例如文件名为```my-awesome-picture.jpg```, 那么文章中引用时只需要直接引用该文件名:

```markdown
![some comment](my-awesome-picture.jpg)
```

就可以正常显示了!

### 误区(重点!)

很多其他的博主会提供该问题的解决办法, 他们会推荐安装```hexo-asset-image```这个插件, 这也是搞的我痛不欲生的原因, 事实证明在当前这个Hexo的版本下是不需要该插件就能正常运行的!
当然猜测可能是由于环境不同或者是老版本的Hexo没有能够正常解决图片的问题, 但是如果你的环境及版本和我一样, 那么希望这篇文章可以帮到你!

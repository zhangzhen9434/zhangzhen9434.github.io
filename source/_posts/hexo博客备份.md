使用Hexo在github搭建的博客，博客作为一个单独的GitHub仓库存在，但是这个仓库只有生成的静态网页文件，并没有Hexo的源文件，如果要换电脑或者重装系统后，就比较麻烦了，这里推荐一种方法。

<!-- more -->

### 备份

1. 在你的仓库username.github.io中创建分支hexo；例如[zhangzhen9434.github.io](https://zhangzhen9434.github.io/)
2. 设置hexo为默认分支；
3. 将刚刚创建的hexo分支`clone`至本地，将之前本地blog文件夹中的`_config.yml`，`themes/`，`source/`，`scaffolds/`，`package.json`，`.gitignore`复制至clone下来的username.github.io文件夹中，在username.github.io文件夹执行`npm install`和`npm install hexo-deployer-git`（这里可以看一看分支是不是显示为hexo）；
4. 将themes/next/(我用的是NexT主题)中的`.git/`删除，否则无法将主题文件夹push；
5. 在WincerChan.github.io文件夹执行`npm install`和`npm install hexo-deployer-git`（这里可以看一看分支是不是显示为hexo）；
6. 执行`git add .`、`git commit -m "update"`、`git push origin hexo`来提交hexo网站源文件；
7. 执行`hexo g -d`生成静态网页部署至Github上。



这样一来，例如[zhangzhen9434.github.io](https://zhangzhen9434.github.io/)仓库就有master分支和hexo分支，分别保存静态网页和源文件。



### 修改

在本地对博客修改（包括修改主题样式、发布新文章等）后：

1. 依次执行`git add .`、`git commit -m ""`、`git push origin hexo`来提交hexo网站源文件；
2. 执行`hexo g -d`生成静态网页部署至Github上。

即重复备份的7-8步骤，以上两部没有严格的顺序。



categories: 

- hexo  
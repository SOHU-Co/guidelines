guidelines
==========

搜狐媒体产品技术中心编码规范

----

## 通用项

- HTML、CSS、Javascript 全部使用**2格缩进**。
- 文件名采用`REST`风格，使用**复数名词**，**小写**，如存在层级关系则放入子目录中，使用`-`单词，例如：
  - users.html
  - users/(**index**|create|update|delete|list).html
  - ~~upload-to-cdn.js~~ (尽量避免，可以使用*upload.js*代替)
- 变量名全部使用**全写**，**禁止使用拼音**。
- 文档全部使用采用`Markdown`。
- （不强制）并尽量保持**80列宽**。

----

## Javascript

- 变量命名使用驼峰规则。

### 后端

- 提交代码前应删除所有`console.log()`，使用[debug](https://github.com/visionmedia/debug)保留必要的log。
- 模板引擎使用[ejs](https://github.com/tj/ejs)。

### 前端

- 提交代码前应删除所有`console.log()`。
- 模板引擎使用[doT](https://github.com/olado/doT)，模板所在`<script>`标签应标记`type="text/x-template-dot"`。
- 需要双向绑定时，使用[angular](https://github.com/angular/angular)。
- 第三方依赖项应使用[bower](https://github.com/bower/bower)安装，并将目录加入到`.gitignore`中。

----

## CSS

- 变量命名使用**减号**`-`分割。

----

## HTML

- 使用`location.hash`对前端页面进行路由。路由规则采用`REST`风格，**并以`#!/`开头**，例如：
  - users.html#!/1
  - users.html#!/1/update
- 避免使用`id`。

----

## 可选资源

- [vim/sublime/.editorconfig/tmux 配置文件](https://github.com/crzidea/vimrc)
- [Gruntfile.js 模板](https://github.com/yeoman/yeoman.io/blob/master/Gruntfile.js)
- [debug 日志调试库](https://github.com/visionmedia/debug)
- [yo](https://github.com/yeoman/yo)

guidelines
==========

搜狐媒体产品技术中心编码规范

----

## 通用项

- HTML、CSS、Javascript 全部使用**2格缩进**。
- 文件名采用`REST`风格，使用**复数名词**，**小写**，如存在层级关系则放入子目录中，使用`-`分割单词，例如：
  - users.html
  - users/(**index**|create|update|delete|list).html
  - ~~upload-to-cdn.js~~ (尽量避免，可以使用*upload.js*代替)
- 变量名全部使用**全写**，**禁止使用拼音**。
- 文档全部使用采用`Markdown`编写。
- （不强制）尽量保持**80列宽**。

----

## Javascript

- 代码风格基本沿用[npm's "funny" coding style](https://docs.npmjs.com/misc/coding-style)。
- 字符串一律使用**单引号**。

特别说明：

  - 类、变量与字段的命名规则
    - 避免使用复杂的继承，**类**名使用驼峰规则，并以大写字母开头，例如：`UpperCamelCase`。
    - 代码中声明的**变量**使用驼峰规则，并以小写字母开头，例如：`lowerCamelCase`。
    - 从数据库、接口输入或输出的**字段**使用下划线分割的规则，并全部小写，例如：`field_from_database`。
  - 异步与回调
    - 异步的方法与回调，传入与传出的参数尽量不要超过**3个**。
    - 异步的方法中最后一个参数应是回调。
    - 回调中第一个参数应是`Error`的子类或`null`。
  - 不强制使用逗号前置的规则。

### 后端

- 提交代码前应删除所有`console.log()`，使用[debug](https://github.com/visionmedia/debug)保留必要的log。
- 模板引擎使用[ejs](https://github.com/tj/ejs)。
- 缓存（*redis/memcache*）的键名应使用REST风格，并以`:`作为分隔符。
- HTTP接口返回的状态码应该清楚明确，出错时应该能讲客户端错误与服务端错误明确的区分开，详见:
  [Status Code Definitions](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)。
- **禁止使用状态码301**。

### 前端

- 提交代码前应删除所有`console.log()`。
- 模板引擎使用[doT](https://github.com/olado/doT)，模板所在`<script>`标签应标记`type="text/x-template-dot"`。
- 需要双向绑定时，使用[angular](https://github.com/angular/angular)。
- 第三方依赖项应使用[bower](https://github.com/bower/bower)安装，并将目录加入到`.gitignore`中。

----

## CSS

- 类名全部使用**小写**，**减号**`-`分割。
- **避免**使用`id`选择器。

----

## HTML

- 使用`location.hash`对前端页面进行路由。路由规则采用`REST`风格，**并以`#!/`开头**，例如：
  - users.html#!/1
  - users.html#!/1/update
- **避免**使用`id`和页内锚点。
- 错误页应以HTTP状态码命名文件，例如：404.html。
- 自定义的标签属性，以`data-`开头，**减号**`-`分割，例如：`data-user-city="beijing"`。

----

## 可选资源

- [vim/sublime/.editorconfig/tmux 配置文件](https://github.com/crzidea/vimrc)
- [Gruntfile.js 模板](https://github.com/yeoman/yeoman.io/blob/master/Gruntfile.js)
- [debug 日志调试库](https://github.com/visionmedia/debug)
- [yo](https://github.com/yeoman/yo)

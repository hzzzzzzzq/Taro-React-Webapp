# Taro-React-Weapp
Taro框架的安装和使用，教你如何用react搭建微信小程序 !

## CLI工具安装

如果安装过程出现 `sass` 相关的安装错误，请在安装 [mirror-config-china](https://www.npmjs.com/package/mirror-config-china) 后重试。

```shell
# 先安装了错误的问题
npm install -g mirror-config-china
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/2021042311113572.png)
- 安装 CLI
```shell
# 使用 npm 安装 CLI
npm install -g @tarojs/cli

# OR 使用 yarn 安装 CLI
yarn global add @tarojs/cli

# OR 安装了 cnpm，使用 cnpm 安装 CLI
cnpm install -g @tarojs/cli
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423111143383.png)
- 查询安装结果
```shell
# 查询安装结果
npm info @tarojs/cli
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423111217410.png)

### Taro小程序搭建

项目初始化，类似于 `react` 的脚手架搭建一个项目

- 初始化一个项目
```shell
# 初始化一个项目
taro init myApp
```

因为首次安装有权限，所以 `sudo` 了一下

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423111223957.png)![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423111536549.png)

如果上面运行的 `yarn install` 失败了 那就自己 `cd` 到项目，手动执行。
```shell
cd myApp
# 然后手动执行
npm install 
# or use yarn
yarn install
```

### 小程序开发

接下俩我们就可以进行小程序的开发了。

下载并打开[微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)，然后选择**项目根目录**进行预览。

需要注意开发者工具的项目设置：

- 需要设置关闭 ES6 转 ES5 功能，开启可能报错
- 需要设置关闭上传代码时样式自动补全，开启可能报错
- 需要设置关闭代码压缩上传，开启可能报错![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423111239521.png)


将我们的项目打开，然后执行编译命令 
```shell
npm run dev:weapp
npm run build:weapp
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423111229858.png)

## 解决版本不匹配问题
这里使用了 `node` 的版本管理模块 `n`

#### 可能遇到了一个问题

`[Node Sass does not yet support your current environment: OS X 64-bit with Unsupported runtime (72)](https://stackoverflow.com/questions/60065790/node-sass-does-not-yet-support-your-current-environment-os-x-64-bit-with-unsupp)`

这个问题是因为，`node-sass` 版本跟 `node` 版本不匹配。[node-sass支持的node版本查看](https://github.com/sass/node-sass/releases/tag/v4.14.1)

#### 解决方案

```shell
# 安装 node 版本管理模块 n
sudo npm install n -g
# 安装 稳定版的 node
sudo n stable 
# 安装 最新的 node
# sudo n latest
# 升级或者降低版本使用
# sudo n 版本号
```

这里就直接安装稳定版本就可以了

安装完之后，查看已经安装版本

```shell
n
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210423112236724.png)

如果安装了好几个，使用 `n 版本号` 就可以切换版本

```shell
# n 版本号
```

删除使用

```shell
sudo n rm 版本号
```

这之后你就可以修改页面，进行开发了，主文件是在 `src-pages-index-index.jsx` 中。



上述就是全部内容了，感谢各位观看

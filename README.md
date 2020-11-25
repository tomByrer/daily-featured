# 每日一荐

![历史共访问次数](https://visitor-count-badge.herokuapp.com/total.svg?repo_id=azl397985856.daily-featured)
![今天被访问次数](https://visitor-count-badge.herokuapp.com/today.svg?repo_id=azl397985856.daily-featured)

> 统计数据的时间是从 2019-09-15 16:50 起至今

![](https://tva1.sinaimg.cn/large/006y8mN6ly1g8d0sktqrwj30hs07maae.jpg)

每天给你推荐一个新奇，好玩，高品质的开源库，好文，观点或言论等。

> 项目主页维护当前月份的内容，想看往期内容，可以翻到下方历史汇总部分，然后选择自己感兴趣的月份点进去即可。

在线阅读：https://leetcode-solution-leetcode-pp.gitbook.io/mz-ri-yi-jm/

电子书文件太大， 大家可到我的公众号《脑洞前端》回复“每日一荐”获取。

## 新鲜出炉 (2020-11)

### 2020-11-25[仓库]

这里有一个测试你 JS 基础能力的系列试题。我做了一下，难度偏简单，更多的还是科普。如果你基础比较差建议看一下。目前有五大块内容：

![](https://tva1.sinaimg.cn/large/0081Kckwly1gl1qpggbtpj30ih07vt95.jpg)

仓库地址：https://github.com/sadanandpai/javascript-code-challenges

### 2020-11-20[好文]

Rust 最近随着 deno 以及其他前端工具的崛起进入了大家的视野。这里有一份 Rust 的教学博客，内容会持续更新，目前有一篇已经翻译成了中文。

地址：https://github.com/pretzelhammer/rust-blog

### 2020-11-19[工具]

fd 是一个可以代替 find 命令的工具命令，使用起来非常简单，而且速度很快。比如:

```
#  查找隐藏文件
fd --hidden
# 查找包括 x 的文件和文件夹
fd x
# 查找 md 后缀的文件
fd -e md
```

等等。。。

mac 用户可以直接 `brew install fd` 安装，其他系统参考下方链接的 install 部分。

地址：https://github.com/sharkdp/fd

### 2020-11-18[技能]

一些 emoji 点缀会使得页面焕发生机。这里列举了 Github 支持的 Markdown emoji 标记，也就是说你可以编辑 markdown 在 Github 看效果。

![](https://tva1.sinaimg.cn/large/0081Kckwly1gktiihfn6jj30qj0kfwic.jpg)

上图是我给我的 [leetcode 仓库](https://github.com/azl397985856/leetcode)增加的 emoji。

地址：https://gist.github.com/rxaviers/7360908

### 2020-11-16[工具]

如果你做一个网站，那么首先要考虑的是用户注册登录这些东西。一个公司都会有自己的账户系统，各个系统进行对接，也就是我们常说的单点登录（SSO）。

这里推荐一个集成账户系统，认证模块，第三方登录，SSO 等的一体化解决方案 Authing。

地址：https://docs.authing.cn/quickstart/best-practise.html

### 2020-11-10[好文]

文章标题《底层原理：垃圾回收算法是如何设计的？》。这是一篇阿里技术出品的 JVM 的垃圾回收算法的底层解析，讲的还是不错的。目前比较流行的算法是标记清除，即从根部可达节点做一次深度优先遍历，将不可达的节点回收。除此之外，垃圾回收还有很多其他细节，比如垃圾回收算法和业务代码是串行，并行，还是并发等，标记和清除是分开的两个步骤么等等。这篇文章会给你答案。

> 其实其他编程语言的 GC 原理都大差不大， 比如 V8 的 GC 就和 JVM 有很多的相似性。

原文链接：https://mp.weixin.qq.com/s/iklfWLmSD4XMAKmFcffp9g

### 2020-11-09[技巧]

以前都不知道 markdown 还可以支持 diff 效果。

以前我只知道可以写代码块，比如：

\`\`\`java

// 你的代码

\`\`\`

可以高亮 java 代码。

而实际上，我们不仅可以写编程语言， 还可以写 diff 实现 diff 效果。

比如：

![](https://tva1.sinaimg.cn/large/0081Kckwly1gkfkk3n9tpj30gr050jri.jpg)

会被渲染为：

```diff
function addTwoNumbers (num1, num2) {
-  return 1 + 2
+  return num1 + num2
}
```

### 2020-11-06[工具]

lighthouse 大家应该都比较熟悉了。 由于不可抗力，国内很多公司都使用 puppeteer + lighthouse 来搭建公司内部的性能评估平台。

一些公司甚至将 lighthouse 的魔改版加入到了公司的构建流程中来了，而 Chrome 官方开源的 lighthouse + ci 来了，不用自己搭建啦~

![](https://tva1.sinaimg.cn/large/0081Kckwly1gkee9gqo42j30ob0hfgpe.jpg)

你如果用 github ，那么集成 lighthouse ci 简直不要太简单，真的是福音啊~

```yml
name: CI
on: [push]
jobs:
  lighthouseci:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v1
      - run: npm install && npm install -g @lhci/cli@0.6.x
      - run: npm run build
      - run: lhci autorun
```

地址：https://github.com/GoogleChrome/lighthouse-ci

### 2020-11-05(好文)

一个面向初级前端的好文，图文并茂，甚至配了动画，生动形象，基本上属于看了就会系列了。

文章讲了什么是垃圾回收以及垃圾回收的两种算法：引用计数和标记清除。还讲了内存泄漏相关的实践内容。

![](https://tva1.sinaimg.cn/large/0081Kckwly1gkecvqx32zj30m80brt9u.jpg)

文章地址：https://felixgerschau.com/javascript-memory-management/

### 2020-11-04[技巧]

很多国人碰到过 node-saas 按照失败的情况，今天介绍一个方法给大家。这个方法其实很简单，使用中国镜像按照即可，比如你用的是 npm，执行以下命令即可：

```bash
npm install -g mirror-config-china --registry=http://registry.npm.taobao.org
npm install node-sass
```

### 2020-11-03[组件库]

当你想使用一些偏门的组件，比如水印，高德地图，音视频等，那么可以考虑使用这个组件库。它是由阿里内部维护开源的，质量应该不错の。

![](https://tva1.sinaimg.cn/large/0081Kckwly1gked9ow3hrj31cr0nh17z.jpg)
（直播组件）

![](https://tva1.sinaimg.cn/large/0081Kckwly1gkeda9fyk7j312z0k6tsb.jpg)
（地图组件）

仓库地址：https://github.com/pansyjs/react-components

## 历史汇总

- [2020-09](./backup/2020-09/README.md)
- [2020-08](./backup/2020-08/README.md)
- [2020-05](./backup/2020-05/README.md)
- [2020-04](./backup/2020-04/README.md)
- [2020-03](./backup/2020-03/README.md)
- [2020-02](./backup/2020-02/README.md)
- [2020-01](./backup/2020-01/README.md)
- [2019-12](./backup/2019-12/README.md)
- [2019-11](./backup/2019-11/README.md)
- [2019-10](./backup/2019-10/README.md)
- [2019-09](./backup/2019-09/README.md)

## 关注我

我重新整理了下自己的公众号，并且我还给它换了一个名字`脑洞前端`，它是一个帮助你打开大前端新世界大门的钥匙 🔑，在这里你可以听到新奇的观点，看到一些技术尝新，还会收到系统性总结和思考。

在这里我会尽量通过图的形式来阐述一些概念和逻辑，帮助大家快速理解，图解是我的目标。

之后我的文章会同步到微信公众号 `脑洞前端` ，你可以关注获取最新的文章，并和我进行交流。

另外你可以回复大前端进大前端微信交流群， 回复 leetcode 拉你进 leetcode 微信群，如果想加入 qq 群，请回复 qq。

<img width="300" src="https://tva1.sinaimg.cn/large/006y8mN6ly1g7he9xdtmyj30by0byaac.jpg">

## 贡献

- 如果有想法和创意，请提 [issue](https://github.com/azl397985856/daily-featured/issues) 或者进群提
- 如果想贡献代码，请提 [PR](https://github.com/azl397985856/daily-featured/pulls)
- 如果需要修改项目中图片，[这里](./assets/) 存放了项目中绘制图的源代码， 大家可以用 [draw.io](https://www.draw.io/) 打开进行编辑。

## License

[Apache-2.0](./LICENSE)

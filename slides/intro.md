---
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://gitee.com/yzketx/image-markdown/raw/master/img/202203171930584.jpg
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# persist drawings in exports and build
drawings:
  persist: false
# download pdf
# download: true
---

# 鸽子广场

浙商大师生交流平台，聚焦浙商大新闻，提供校内小工具

王俊涵 叶泽楷 林悦章

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    咕咕咕 <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/bigcheeses" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---
layout: cover
background: https://gitee.com/yzketx/image-markdown/raw/master/img/202203180951574.png
---

# 项目背景

解决师生对校园等大事的社交欲望，拢合校园新闻

---
layout: cover
background: https://gitee.com/yzketx/image-markdown/raw/master/img/202203081856107.png
---

# 思维导图

浙商大师生交流平台，聚焦浙商大新闻，提供校内小工具

<img
  v-click
  class="absolute -bottom-0 -right-50 w-80 opacity-100"
  src="https://sli.dev/assets/arrow-bottom-left.svg"
/>
<p v-after class="absolute bottom-20 right-20 opacity-45 transform -rotate-20">详情请点这里!</p>

<div class="abs-br m-6 flex gap-2">
  <a href="https://gitee.com/yzketx/image-markdown/raw/master/img/202203081856107.png" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-60 !border-none !hover:text-black">
    <carbon:airplay />
  </a>
</div>

---
layout: image-right
image: https://gitee.com/yzketx/image-markdown/raw/master/img/202203171937790.png
---

#  用户

| 功能         | 接口 (/user^)     | 描述                     |
| ------------ | ----------------- | ------------------------ |
| 登录/登出    | /login    /logout |                          |
| 注册         | /register         |                          |
| 修改密码     | /change_password  |                          |
| 第三方登入   | /third-auth       | 待定                     |
| 修改个人信息 | /profile          |                          |
| 个人简介     | /intro            | 公开信息           |
| 课程表       | /school-timetable | 上传信息           |
| 浏览记录     | /history          | 动态\|新闻 |

<div class="abs-br m-6 flex gap-2">
  <a href="https://gitee.com/yzketx/image-markdown/raw/master/img/202203171937790.png" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-60 !border-none !hover:text-black">
    <carbon:airplay />
  </a>
</div>

---
layout: image-right
image: https://gitee.com/yzketx/image-markdown/raw/master/img/202203172003335.png
---

# 动态

| 功能      | 接口 (/moment^) | 描述 |
| --------- | --------------- | ---- |
| 发布      | post方法        |      |
| 详情/简介  | get方法         |      |
| 简介      | /intro          |      |
| 标签      | /tag            |      |
| 评论      | /comment        |      |
| 点赞      | /like           |      |
| 收藏      | /star           |      |
| 关注      | /follow         |      |
| 搜索      | /search         |      |
| 分享      | /share          |      |

<div class="abs-br m-6 flex gap-2">
  <a href="https://gitee.com/yzketx/image-markdown/raw/master/img/202203172003335.png" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-60 !border-none !hover:text-black">
    <carbon:airplay />
  </a>
</div>

---
layout: image-right
image: https://gitee.com/yzketx/image-markdown/raw/master/img/202203172033268.png
---

# 新闻

| 功能               | 接口 (/news^)   | 描述                 |
| ------------------ | --------------- | -------------------- |
| 点赞               | /like           |                      |
| 分享               | /share          |                      |
| 抓取新闻            | 纯后端           | 获取微信公众号        |
| 详情              | get方法         |                      |
| 简介               | /intro          |                      |
| 评论               | /comment        |                      |

<div class="abs-br m-6 flex gap-2">
  <a href="https://gitee.com/yzketx/image-markdown/raw/master/img/202203172033268.png" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-60 !border-none !hover:text-black">
    <carbon:airplay />
  </a>
</div>

---
layout: image-right
image: https://gitee.com/yzketx/image-markdown/raw/master/img/202203172018491.png
---

# 消息

| 功能             | 接口                                 | 描述 |
| ---------------- | ------------------------------------ | ---- |
| 我的评论          | /user/comment                      | 待定     |
| @我评论           | /user/commented                    |     |
| 被点赞            |  /user/liked                       |      |
| 点赞              | /user/like                         |      |
| 私聊              | /message                           |      |

<div class="abs-br m-6 flex gap-2">
  <a href="https://gitee.com/yzketx/image-markdown/raw/master/img/202203172018491.png" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-60 !border-none !hover:text-black">
    <carbon:airplay />
  </a>
</div>

---

# Django

Django makes it easier to build better web apps more quickly and with less code.

`Restful API` `MTV` `Postgresql`
<br>

- 🎨 **强大的缓存支持** - 内置了缓存框架，并提供了多种可选的缓存方式

- 🤹 **灵活的URL映射** - 提供基于正则表达式的URL分发器，开发者可灵活地编写URL

- 📝 **齐全的功能** - 自带大量常用工具和框架，可轻松、迅速开发出功能齐全的Web应用

- 🎥 **丰富的模板语言** - 模板语言功能丰富，支持自定义模板标签，也支持使用第三方模板系统，如jinja2等

- 🧑‍💻 **强大的数据库访问组件** - 自带面向对象的、反映数据模型与关系型数据库间的映射关系的映射器(ORM)

- 🛠 **完整的错误信息提示** - 提供完整的错误信息提示和定位功能，可在开发调试过程中快速定位错误或异常

- 📤 **健全的后台管理系统** - 内置后台数据管理系统，经简单配置，编写少量代码即可使用完整的后台管理功能

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# Android

`MVP`

<img src="https://gitee.com/yzketx/image-markdown/raw/master/img/202203172353278.webp" alt="img" style="zoom:50%;" />

Presenter：连接View层与Model层的桥梁并对业务逻辑进行处理。

View：视图层，在View层中只负责对数据的展示，提供友好的界面与用户进行交互。

Model：数据层。负责对数据的存取操作，例如对数据库的读写，网络的数据的请求等。

- 模型与视图完全分离，我们可以修改视图而不影响模型
- 可以更高效地使用模型，因为所有的交互都发生在一个地方——Presenter内部
- 我们可以将一个Presenter用于多个视图，而不需要改变Presenter的逻辑
- 逻辑结构更加清晰，解决Activity代码臃肿问题

[APP完整设计链接](https://js.design/f/Kh8vOZ?p=p4NfHwUO5n)

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
preload: false
---

# Power by Slidev

<br>
<br>
<br>

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-square.png"
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-triangle.png"
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 40, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

</div>

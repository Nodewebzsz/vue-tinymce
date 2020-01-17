# 使用细节

## 本地化

以vue-cli为例，先去[这里](https://www.tiny.cloud/get-tiny/language-packages/)下载`zh_CN`语言包，然后放置到`public/tinymce/langs/zh_CN.js`，然后在编辑器中设置下面内容就能实现本地化处理。

```js
{
    language: "zh_CN",
    language_url: "/tinymce/langs/zh_CN.js" //使用language_url会相对灵活
}
```

> 注意：至tinymce v5.1.5版本为止，页面存在多个编辑器时本地化设置无法根据单个编辑器进行处理。可以看这个例子动手尝试：[传送门](https://codepen.io/packy1980/pen/zYxagWR)

## 推荐设置

提供一个脚手架设置作为参考，👇最下面附上设计说明。

```js
const scaffold_settings = {
    menubar: false,
    toolbar: "undo redo | fullscreen | formatselect alignleft aligncenter alignright alignjustify | link unlink | numlist bullist | image media table | fontselect fontsizeselect forecolor backcolor | bold italic underline strikethrough | indent outdent | superscript subscript | removeformat |",
    toolbar_drawer: "sliding",
    quickbars_selection_toolbar: "removeformat | bold italic underline strikethrough | fontsizeselect forecolor backcolor",
    plugins: "link image media table lists fullscreen quickbars",
    language: 'zh_CN',
    language_url: 'https://lab.uxfeel.com/node_modules/tinymce/langs/zh_CN.js'
}
```

<iframe height="450" style="width: 100%;" scrolling="no" title="TinyMCE5.x_CommonSettings" src="https://codepen.io/packy1980/embed/BayPrVO?height=265&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/packy1980/pen/BayPrVO'>TinyMCE5.x_CommonSettings</a> by packy
  (<a href='https://codepen.io/packy1980'>@packy1980</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## 插入图片

<iframe height="500" style="width: 100%;" scrolling="no" title="TinyMCE5.x_InsertImage" src="https://codepen.io/packy1980/embed/VwYGpVE?height=500&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/packy1980/pen/VwYGpVE'>TinyMCE5.x_InsertImage</a> by packy
  (<a href='https://codepen.io/packy1980'>@packy1980</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## 转换表情图片

<iframe height="500" style="width: 100%;" scrolling="no" title="TinyMCE5.x_EmotionsExample" src="https://codepen.io/packy1980/embed/oNgPrqx?height=500&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/packy1980/pen/oNgPrqx'>TinyMCE5.x_EmotionsExample</a> by packy
  (<a href='https://codepen.io/packy1980'>@packy1980</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

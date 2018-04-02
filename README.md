## hulogb

[Hugo](https://gohugo.io/) + [Netlify](https://www.netlify.com/), with [hugo-theme-even](https://github.com/olOwOlo/hugo-theme-even)

Click this button:
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/kuleyu/hulogb/)

添加[搜索功能](https://gist.github.com/eddiewebb/735feb48f50f0ddd65ae5606a1cb41ae)时,踩了一个坑：`index.json` 文件，应该改成 `search.json` 。只有这样，生成的 `index.json` 文件才会在 `/search/index.json` 路径中，这时才会被 `search.js` 中`$.getJSON( "/search/index.json", function( data ) {......}）`正确的查询。总之路径要对应起来（前者生成的 `index.json` 文件会在根目录中，以至于生成了但匹配不到）。

这个问题的根本原因应该在于 `Even` 主题本身内部的一些路径不统一问题，一旦以某个特定的`site`地址来 `deploy` 就会造成路径不一样。

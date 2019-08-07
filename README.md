# Bookcase
save your book and reading condition online

## 将Bookcase嵌入自己的网页
``` html
<iframe id="iframe"
        allowtransparency="true"
        frameborder="0"
        scrolling="yes"
        tabindex="0"
        width="100%"
        horizontalscrolling="no"
        verticalscrolling="no"
        style="width: 1px !important;
                min-width: 100% !important;
                border: none !important;
                overflow: hidden !important;
                min-height: 300px"
        src="index.html"></iframe>
<script>
    window.setInterval(() => {
        try {
            var iframe = document.getElementById("iframe")
            iframe.height = 0
            iframe.height =
                Math.max(iframe.contentWindow.document.body.scrollHeight,
                    iframe.contentWindow.document.documentElement.scrollHeight)
        } catch (ex) {
        }
    }, 20)
</script>
```
注意修改上面iframe的src属性来连接到正确的网页
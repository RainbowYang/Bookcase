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
        src="https://bookcase.rainbowyang.moe/"></iframe>
<script>
    document.domain="rainbowyang.moe" //for cross origin
    window.setInterval(() => {
        try {
            var iframe = document.getElementById("iframe")
            console.log(iframe.contentWindow.document.body.scrollHeight)
            console.log(iframe.contentWindow.document.documentElement.scrollHeight)
            iframe.height =
                Math.max(iframe.contentWindow.document.body.scrollHeight,
                    iframe.contentWindow.document.documentElement.scrollHeight)
        } catch (ex) {
            console.log(ex)
        }
    }, 20)
</script>
```
注意修改上面iframe的src属性来连接到正确的网页
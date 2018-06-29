# img src-set & sizes

## `w` 參數

`w` 參數指的是圖片的寬度，瀏覽器會針對裝置的寬高去做圖片 Responsive 的判斷

```html
<img src="source_min.jpg" width="100%"
     srcset="source_width_400.jpg 400w,
            source_width_600.jpg 600w,
            source_width_1280.jpg 1280w"
/>
```

## `sizes` 參數


```html
<img src="source_min.jpg"
     width="100%"
     srcset="source_width_400.jpg 400w,
            source_width_600.jpg 600w,
            source_width_1280.jpg 1280w"

     sizes="(max-width: 320px) 280px,
            (max-width: 480px) 440px,
            800px"
/>
```

*`sizes` 流程*

1. 檢查裝置寬度（包含裝置像素密度）
2. 檢查是否符合 `sizes` 中的 Media query：`(max-width: 320px)`
3. 將符合 Media query 條件後面的 `slot size` 設定為目前圖片寬度
4. 載入 `srcset` 中最接近 `slot size` 的圖片


## 參考資料
* [借助 srcset、sizes 和 heights 属性制作自适应图片 – AMP](https://www.ampproject.org/zh_cn/docs/design/responsive/art_direction)
* [用 srcset 屬性做簡單的 Responsive Image « The Front Row](http://blog.zhusee.in/post/248199/basic-responsive-image-with-srcset-property)
* [Responsive images - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
* [Image srcset attribute example](https://webkit.org/demos/srcset/)
* [Can I use... srcset](https://caniuse.com/#search=srcset)
* [Srcset and sizes — ericportis.com](https://ericportis.com/posts/2014/srcset-sizes/)
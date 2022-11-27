# 微信小程序EXIF.js

## 安装
下载项目中的exif.js文件到项目文件夹

## 使用
```javascript
import { getImageData } from '/path/to/exif.js'
wx.chooseImage({
  count: 1,
  sourceType: ['album', 'camera'],
  success (res) {
    const tempFilePaths = res.tempFilePaths
    getImageData(tempFilePaths).then(exifData => {
        console.log(exifData)
    }).catch(error => {
        console.log(error)
    })
  }
})
```
# Cocos creator 1.9.3

muốn sửa core của *Cocos creator* thì phải build project dạng *link*
sau khi sửa core xong cần phải build lại libs để các project build dạng *binary*

tham khảo link sau để biết cách build
http://cocos2d-x.org/docs/cocos2d-x/en/editors_and_tools/prebuilt_libraries.html?h=gen-libs

build lib command
```
cocos gen-libs -p ios
```

sau khi build lại libs nó sẽ sinh ra ở thư mục này
```
/Applications/CocosCreator.app/Contents/Resources/cocos2d-x/prebuilt/ios
```

# Cài đặt

Phải add thêm 2 thư viện vào project
```
CoreMedia.framework
AVKit.framework
```

## Cài đặt cho toàn bộ các project

copy thư mục *ios* vào thư mục
```
/Applications/CocosCreator.app/Contents/Resources/cocos2d-x/prebuilt/ios
```

từ nay về sau các project được build dạng *binary* nó sẽ lấy libs ở trong thư mục này

## Cài đặt cho project đơn lẻ
Sau khi build project từ *cocos creator* mở = xcode rồi kéo 2 file *libcocos2d iOS.a, libjscocos2d iOS.a* vào thư mục *ios-libs* 

HOÀN TẤT QUÁ TRÌNH CÀI ĐẶT

lấy libs build sẵn + project demo ở đây:
https://drive.google.com/drive/u/0/folders/1YwH2Myg_tb9CwpJVPQ0HJA_3c5pwqezO


# Note
*cocos creator* hiện đang sử dụng *MPMoviePlayerController* để phát video, nó không được sử dụng trong iOS 9 nữa
và nó ko thể phát video ở thư mục Documents của ứng dụng

> The MPMoviePlayerController class is formally deprecated in iOS 9. (The MPMoviePlayerViewController class is also formally deprecated.) To play video content in iOS 9 and later, instead use the AVPictureInPictureController or AVPlayerViewController class from the AVKit framework, or the WKWebView class from WebKit.

Hiện đã có bug và đã có giải pháp thay thế

issue: https://github.com/cocos2d/cocos2d-x/issues/17887

giải pháp: https://github.com/cocos2d/cocos2d-x/pull/18467
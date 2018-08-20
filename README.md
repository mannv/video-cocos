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

# Cài đạt

## Cài đặt cho toàn bộ các project

copy thư mục *ios* vào thư mục
```
/Applications/CocosCreator.app/Contents/Resources/cocos2d-x/prebuilt/ios
```

từ nay về sau các project được build dạng *binary* nó sẽ lấy libs ở trong thư mục này

## Cài đặt cho project đơn lẻ
Sau khi build project từ *cocos creator* mở = xcode rồi kéo 2 file *libcocos2d iOS.a, libjscocos2d iOS.a* vào thư mục *ios-libs* 

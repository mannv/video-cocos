# Cocos creator 1.9.3

muốn sửa core của *Cocos creator* thì phải build project dạng *link*
sau khi sửa core xong cần phải build lại libs để các project build dạng *binary*

tham khảo link sau để biết cách build
http://cocos2d-x.org/docs/cocos2d-x/en/editors_and_tools/prebuilt_libraries.html?h=gen-libs

build lib command
```
cocos gen-libs -p android --app-abi armeabi-v7a
```

sau khi build lại libs nó sẽ sinh ra ở thư mục này
```
/Applications/CocosCreator.app/Contents/Resources/cocos2d-x/prebuilt/ios
```

# Cài đặt

1. sau khi build project từ *cocos creator* chạy compile lần đầu
```
cocos compile -p android --android-studio --no-apk
```

2. mở project = *android studio*

- replace các file sau ở trong projects *libcocos2dx*
```
Cocos2dxActivity.java
Cocos2dxVideoHelper.java
Cocos2dxVideoView.java
```

- copy nút close + view cho nút close
copy toàn bộ thư mục *res* vào project của *libcocos2dx*

HOÀN TẤT QUÁ TRÌNH CÀI ĐẶT

lấy libs build sẵn + project demo ở đây:
https://drive.google.com/drive/u/0/folders/1YwH2Myg_tb9CwpJVPQ0HJA_3c5pwqezO

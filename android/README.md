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

```
thực chất thằng *cocos creator* build android nó ko sử dụng file libs thì phải
```

1. mở file
```
./build/jsb-binary/frameworks/runtime-src/proj.ios_mac/hello_world.xcodeproj
```


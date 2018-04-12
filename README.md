这个demo是使用 [Create React Native App](https://github.com/react-community/create-react-native-app)来创建的.

下面是我本地环境的配置

## 安装npm环境

参考[Node官网](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)来安装

## 配置

- 基本配置
```
npm install -g yarn react-native-cli
yarn config set registry https://registry.npm.taobao.org --global
yarn config set disturl https://npm.taobao.org/dist --global
```

- 添加Android SDK
在.bashrc中添加 
```
 #Android SDK
 export ANDROID_HOME="/home/betterzw/android-sdk"
```
- 创建工程
```
create-react-native-app AwesomeProject
```
- 初始化
```
react-native init AwesomeProject
```
- 运行
```
react-native run-android
```
## 遇到的问题

```
could not get batchedbridge, make sure your bundle is packaged correctly
```

解决
```
mkdir android/app/src/main/assets
react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
```



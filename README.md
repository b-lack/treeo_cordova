# treeo app

## Related Repositories
https://github.com/b-lack/treeo_app  
https://github.com/b-lack/treeo_webview

## Related Application
https://github.com/fxhinze/treeo_admin  
https://github.com/yalsicor/treeo_api

# Install
1. $ npm install
2. $ cordova platform add android

# Test
1. $ cordova run android

# Deploy
1. Change APP-Version (config.xml)
2. $ cordova build --release android
3. $ jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -storepass "password" -keystore /path/to/keystore /path/to/of_treeo_cordova/platforms/android/app/build/outputs/apk/release/app-release-unsigned.apk treeo
4. $ /path/to/Android/Sdk/build-tools/28.0.2/zipalign -v 4 /path/to/of_treeo_cordova/platforms/android/app/build/outputs/apk/release/app-release-unsigned.apk /path/to/of_treeo_cordova/platforms/android/app/build/outputs/apk/release/treeo_v11_auto.apk

# Publish (Play Store)
1. App-Releases -> Create Release
2. Upload /path/to/of_treeo_cordova/platforms/android/app/build/outputs/apk/release/treeo_v11_auto.apk to Play Store

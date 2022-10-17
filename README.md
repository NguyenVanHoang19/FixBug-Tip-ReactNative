# FixBug-Tip-ReactNative

- View List Images React-Native
+ https://github.com/jobtoday/react-native-image-viewing 

--- react-native-image-crop-picker

- unexpected element <queries> found in <manifest>
+ https://github.com/ivpusic/react-native-image-crop-picker/issues/1406

--https://github.com/ivpusic/react-native-image-crop-picker

-- https://www.youtube.com/watch?v=3_ldEVWlL18

  
  
  React Native:
- Create React Native project: npx react-native init MyTestApp
- Create React Native projec with versiont: npx react-native init MyTestApp —version X.XX.X
- Start server: npx react-native start
- Run iOS: npx react-native run-ios
- Run iOS device you want: npx react-native run-iOS -simulator=“iPhone 11 Pro Max” (npx react-native run-ios --simulator 'iPhone 8 Plus’)
- Run Android: npx react-native run-android
- Run Release android: npx react-native run-android --variant=release
- Create debug.keystore (android): keytool -genkey -v -keystore debug.keystore -storepass android -alias androiddebugkey -keypass android -keyalg RSA -keysize 2048 -validity 10000
- Check device connected: adb devices
- Kill server: killall -9 node
- Format code: Shift + Option + F
- Format config: Shift + Cmd + P
- Comment: cmd + /
- Debug iOS :ctrl + cmd + Z (cmd + D)
- Debug android :ctrl + cmd + Z (cmd + M)
- Android studio: http://127.0.0.1, BASE_URL: http://10.0.2.2,
- Jump to end of the line: cmd + left arrow

Change name:
- Android: android/app/src/main/res/values/string.xml change app_name
- iOS: go Info.plist chang “Bundle display name”

Install:
1. React navigation (điều hướng):
- npm install @react-navigation/native
- npm install @react-navigation/stack
- npm install @react-navigation/bottom-tabs
- npm install @react-navigation/material-top-tabs
- npm install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view
- npx pod-install ios
- Add this line at the top of index.js or App.js: import 'react-native-gesture-handler';
  2.  Component (text, button,…):
- npm install react-native-paper
- npm install react-native-vector-icons
- npx pod-install ios
  3. Axios ( call API):
- npm install axios
  4. Safe area (iOS only):
- npm install react-native-safe-area-context
- npx pod-install ios
  5. Swipe list:
- npm install --save react-native-swipe-list-view
  6. Input type:
- npm install react-native-text-input-mask
- Add this line in Podfile (target): pod 'RNInputMask', :path => '../node_modules/react-native-text-input-mask/ios/InputMask'
  7. Item Picker:
- npm install react-native-picker
- npx pod-install
8. WebView (show web on App):
- npm install --save react-native-webview
- cd ios
- rm Podfile.lock
- pod install
9. UI ( react native element):
- npm i react-native-elements --save
- npm i --save react-native-vector-icons
- npx pod-install ios
- react-native link react-native-vector-icons
10. Data time picker:
- npm install @react-native-community/datetimepicker --save
- npx pod-install ios
11. Linear gradient:
- npm install react-native-linear-gradient --save
- npx pod-install
- cd ios
- pod install
12. Camera:
- npm install react-native-camera —save
- npx pod-install ios
- Ex: pod 'Permission-Camera', :path => "#{permissions_path}/Camera.podspec"
- Android: android/app/src/main/AndroidManifest.xml: <uses-permission android:name="android.permission.CAMERA" />
- IOS: iOS/{Project}/Info.plist:     <key>NSCameraUsageDescription</key>
-     <string>YOUR TEXT</string>
13. Scanner (Qrcode, barcode, …):
- npm install react-native-qrcode-scanner --save
- npx pod-install ios
14. Permission:
- npm install react-native-permissions --save
- npx pod -install ios
- Go to Podfile add:
- permissions_path = '../node_modules/react-native-permissions/ios'
15. Format Input:
- npm install react-native-masked-text --save
16. Redux:
- npm install redux react-redux
17. Icon:
- npm i --save react-native-vector-icons
- npx pod-install iOS
- Android: go to android/app/build.gradle add line:apply from: "../../node_modules/react-native-vector-icons/fonts.gradle"
- IOS:  
- add this into in ios/project/info.plit:
<key>UIAppFonts</key>
<array>
<string>AntDesign.ttf</string>
<string>Entypo.ttf</string>
<string>EvilIcons.ttf</string>
<string>Feather.ttf</string>
<string>FontAwesome.ttf</string>
<string>FontAwesome5_Brands.ttf</string>
<string>FontAwesome5_Regular.ttf</string>
<string>FontAwesome5_Solid.ttf</string>
<string>Foundation.ttf</string>
<string>Ionicons.ttf</string>
<string>MaterialIcons.ttf</string>
<string>MaterialCommunityIcons.ttf</string>
<string>SimpleLineIcons.ttf</string>
<string>Octicons.ttf</string>
<string>Zocial.ttf</string>
</array>
- Then open build phase and copy font to “Copy Bundle Resources”
- Old:
- import Icon from 'react-native-vector-icons/FontAwesome'; (not need)
- Icon.loadFont(); (not need)
- And add fonts in node-modules/react-native-vector-icon to info-plot/Font and application in xcode
18. Avoid keyboard:
- npm i react-native-keyboard-aware-scroll-view --save
19. Media (Capture and Picker):
- npm install react-native-image-crop-picker --save
- npx pod-install iOS
- Android:
- <uses-permission android:name="android.permission.CAMERA" />
- <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
- IOS:
- <key>NSMicrophoneUsageDescription</key> <string>Need audio access</string>
- <key>NSPhotoLibraryUsageDescription</key> <string>Need library access to upload images</string>
- <key>NSCameraUsageDescription</key> <string>Need camera access to take pictures</string>
20. Video:
- npm install --save react-native-video
- npx pod-install ios
21. Dialog:
- npm install --save react-native-popup-dialog
22. Gallery ( Show list of photo):
- npm i react-native-grid-image-viewer --save
- Click go to GridImageViewer.js comment all code in useEffect.
23. Video Player ( Manger Video):
- npm install --save react-native-video react-native-video-controls
- npx pod-install ios
24. Add fonts to project:
- Create file react-native.config.js at root folder:
	module.exports = {
  		project: {
    			ios: {},
    			android: {}
  		},
  	assets: ['./src/assets/fonts'],
	};
- Add font to src/assets/fonts.
- npx react-native link
25. Asyn store( Luu tru bat dong bo):
- npm install @react-native-async-storage/async-storage
- npx pod-install iOS
26. OTP:
- npm install --save @twotalltotems/react-native-otp-input
- npm install --save @react-native-community/clipboard
- npx pod-install iOS
27. Select multiple:
- npm install @zenzillo/react-native-select-multiple
- npm install @horizonlime/react-native-select-multiple
28. Checkbox:
- npm install @react-native-community/checkbox
29. Show bottom view:
- npm install reanimated-bottom-sheet —save
30. Sign in Google:
- npm instal @react-native-google-signin/google-signin
31. Sign in Facebook:
- react-native-fbsdk-next
32. UI:
- npm install react-native-elements
- npm install react-native-vector-icons
- npm install react-native-safe-area-context
33. Grid view Item:
- npm install react-native-easy-grid --save
34. Range date time picker:
- npm install rn-select-date-range
- npm install --save moment
35. Share data thought 3rd app:
- npm i react-native-share —save
- npx pod-install ios
Api:
- formData:  body(form-data)
- body: body(raw)
- query: params
Uninstall: npm uninstall --save package_name
Build Release:
- Android ( if you already have keystone and pushed before, you can skip 1->4):
1. keytool -genkeypair -v -keystore my-upload-key.keystore -alias my-key-alias -keyalg RSA -keysize 2048 -validity 10000
2. Move my-key-store.keystore to android/app
3. Config gradle.properties in android:
	MYAPP_UPLOAD_STORE_FILE=my-upload-key.keystore
	MYAPP_UPLOAD_KEY_ALIAS=my-key-alias
	MYAPP_UPLOAD_STORE_PASSWORD=***
	MYAPP_UPLOAD_KEY_PASSWORD=***
  4.Config build.gradle in android/app:
  - In label: android/signingConfigs:
 release {
            if (project.hasProperty('MYAPP_UPLOAD_STORE_FILE')) {
                storeFile file(MYAPP_UPLOAD_STORE_FILE)
                storePassword MYAPP_UPLOAD_STORE_PASSWORD
                keyAlias MYAPP_UPLOAD_KEY_ALIAS
                keyPassword MYAPP_UPLOAD_KEY_PASSWORD
            }
        }
  - In tab: androids/buildTypes/release:
	signingConfig signingConfigs.debug -> release
  5.cd android
  6./gradlew bundleRelease
	Fix warning:
7. Warning react native on Google Play Console:
    1. In android/app/build.gradle add this line on defaultConfig: ndk { debugSymbolLevel 'SYMBOL_TABLE' }
    2. In local.properties add ndk.dir={PATH OF NDK}
8. Warning Java/Kotlin on Google Play Console:
    1. In android/app/build.gradle add this line on buildTypes/release: minifyEnabled true
9. When update new version: - Go to android/app/build.grade - Change versionCode and versionName
- iOS:
1. Go to info.plit -> App Transport Security Settings -> Exception Domains -> localhost, delete it ( default have 1 item is NSExceptionAllowsInsecureHTTPLoads : Boolean 1)
2. Go to Product -> Edit Schema -> Debug to Release
	
Error:
1. Can’t launch Android emulator:
- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
- brew cask install android-platform-tools
- adb devices
  2. Crash when import ‘react-native-gesture-handler’:
- watchman watch-del-all
- npx react-native start —reset-cache
3. Can’t laugh “npx react-native run-android”:
- Create file local.properties in android folder
- sdk.dir=/Users/admin/Library/Android/sdk
4. File when build release Android (duplicate resources):
- Remove ./android/app/src/main/res/raw
5. Keyboard push element on top (Android):
- Add this file AndroidManifest.xml in activity tag : android:windowSoftInputMode="adjustPan"
6. Error front awesome icon on Android:
- Add : apply from: "../../node_modules/react-native-vector-icons/fonts.gradle" after apply plugin: "com.android.application" in app/build.gradle
7. Error about ‘:app:mergeDexDebug’ when build app on Android:
- Go to android/app/build.gradle and add this lines of codes:
android { defaultConfig { multiDexEnabled true }}
8. Downloading Javascript 100% stuck:
- Turn off Debug
9. Deprecated Gradle features were used in this build, making it incompatible with Gradle 7.0
- npx react-native run-android warning-mode=all
10. error: bundling failed: Error: ENOENT: no such file or directory
- killall node
- rm -rf ios/build/ &&  npx react-native run-ios
11. React-native run-android is unrecognized
- npm install.
12. App not register:
- Close metro.
- Run again.
13. Keyboard over layout:
- android:windowSoftInputMode=“adjustResize” -> adjustPan" in AndroidManifest.
14. After pod install, can not run iOS:
Undefined symbol: __swift_FORCE_LOAD_$_swiftUniformTypeIdentifiers Undefined symbol: __swift_FORCE_LOAD_$_swiftCoreMIDI 
Undefined symbol: __swift_FORCE_LOAD_$_swiftWebKit 
- Open Xcode, add empty Swift file to project, build again.
15. app:transformClassesAndResourcesWithR8ForRelease :
- In android/ gradle.properties add :android.enableR8=false
16. app:transformClassesAndResourcesWithProguardForRelease:
- In android/ app/ proguard-rules.pro add: -ignorewarnings
17. Network error when release:
<manifest ...>
    <uses-permission android:name="android.permission.INTERNET" />
    <application
        ...
        android:usesCleartextTraffic="true"  // <-- added this 
        ...>
        ...
    </application>
</manifest>
18. No bundle url present:
- npx react-native bundle --entry-file='index.js' --bundle-output='./ios/main.jsbundle' --dev=false --platform='ios' --assets-dest='./ios'
- Copy file main.bundle to root folder in Xcode.
19. Task :app:mergeExtDexDebug FAILED (java.nio.file.NoSuchFileException:):
- Delete .gradle in android folder
- Nom run android.
20. run-ios old version code:
- npx react-native bundle --entry-file index.js --platform ios --dev false --bundle-output ios/main.jsbundle --assets-dest ios/assets
21. Operator ‘abs’ not found:
- npm install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view
22. Can not connect metro JavaScript:
- Shake your device
- Choose Configure Bundler
- 127.0.0.1:8081
23. Unknown type name bn_ulong:
- pod 'OpenSSL-Universal', '~>1.0.2.20' in Pod.file
- If error when run, delete Podfile.lock and run pod install in iOS folder.
24. :app:installDebug failed (npx react-native run-android):
- Remove old app.
25. INSTALL_FAILED_INSUFFICIENT_STORAGE
- No space to install app.
26. Error when run “npx react-native run-ios”:
- Open Podfile and comment:   use_flipper!
    	post_install do |installer|
    	flipper_post_install(installer)
  	end
27. Unexpected element <queries>found in <manifest>:
- Open android studio and update gradle.
28. Response 500 metro when run: npx react-native run-android
- Delete node_module folder.
- npm install.
29. Task :app:compileDebugJavaWithJavac FAILED:
- In android/gradle/gradle.properties add: org.gradle.java.home=/path_to_jdk_directory
30. Error spawnSync ./gradlew EACCES when running ‘react-native run-android’
- chmod 755 android/gradlew
31. Error with App Transport Security ( this error appear when change local to product)
- Open Info.plist in iOS/project.
<key>NSAppTransportSecurity</key>
<dict>
	//Add this line
	<key>NSAllowsArbitraryLoads</key>
            <true/>
	//Add this line
</dict>


32. Modal bottom
https://github.com/jeremybarbet/react-native-modalize

33. Web logo design
https://www.freepik.com/free-photos-vectors/beauty-logo

34. QR code
https://aboutreact.com/react-native-scan-qr-code/

35. Slider
https://youtu.be/otr_x0wKgvU

https://github1s.com/KPS250/React-Native-FlatList-Slider/blob/HEAD/src/FlatListSlider.js

36. Project example
https://github1s.com/eramudeep/react-native-ecommerce
 37. Scroll layout
https://medium.com/@linjunghsuan/implementing-a-collapsible-header-with-react-native-tab-view-24f15a685e07
38. React nativ rich text editor
https://www.npmjs.com/package/react-native-pell-rich-editor

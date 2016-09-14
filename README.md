
#RESUME: COMMANDS TO GIST

wget http://dl.google.com/android/android-sdk_r24.2-linux.tgz
tar -xvf android-sdk_r24.2-linux.tgz
rm android-sdk_r24.2-linux.tgz
mv android-sdk-linux/ android
~/workspace/android/tools/android update sdk -u --all --filter 2,4,168
sudo apt-get install lib32stdc++6
sudo apt-get install lib32z1
npm install -g cordova ionic@beta
cd ~/workspace

sudo rm -r /home/ubuntu/.gradle/caches/*
sudo rm -r /var/cache/*

ionic start myApp tabs
cd ~/workspace/myApp
cordova plugin add cordova-hot-code-push-plugin
cordova plugin add cordova-hot-code-push-local-dev-addon
npm install -g cordova-hot-code-push-cli
sudo apt-get install lib32stdc++6
sudo apt-get install lib32z1


#space in directory
du -h --max-depth=1 | sort -hr


#ENVIROMENTAL VARIABLES TO ADD

~/.profile

ANDROID_HOME='/home/ubuntu/workspace/android'
PATH="$PATH:$HOME/workspace/android/tools"
PATH="$PATH:$HOME/workspace/android/platform-tools"
PATH="$PATH:$HOME/workspace/android/build-tools"


#IF BUILD FAILED WITH ERRO RELATED TO DEX ADD THAT LINE TO BUNDLE.GRADLE

android {
    defaultConfig {
       multiDexEnabled true  // this line will solve this problem
   }
}

#IF SUCCESS THEN PATH OF APK
/home/ubuntu/workspace/myApp/platforms/android/build/outputs/apk/android-debug.apk


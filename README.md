# livepeer-demo-react-native

This is a demo React Native live streaming application built with the [Livepeer.com API](https://livepeer.com/docs/api). It can serve as a starting point for building cross-platform mobile live streaming apps.

## Installation

```sh
yarn
cd ios && pod install && cd ..
```

## Development

### Android

To run on android simulator, use the following command:

```sh
yarn android
```

### iOS

In order to use the broadcasting functionality, you'll need to run the app on an actual ios device:

```sh
npx react-native run-ios --device DEVICE_NAME
```

If you just want to run the app in a simulator, everything else should still work as intended with the following command:

```sh
yarn ios
```

## Troubleshooting

**pod install is failing**

If you run into issues running `pod install` on macOS, try updating with the following command:

```sh
sudo gem install -n /usr/local/bin cocoapods
```

**`nvm` and XCode 12**

If you run into issues finding `node` during build time, you may be a victim of [this issue](https://github.com/facebook/react-native/issues/31249#issuecomment-811715288).

Commenting out all of the bash code in `node_modules/react-native/scripts/find-node.sh` worked for me, but I also have to remember to do it each time I install a new dependency.

**Assets aren't loading properly**

You may need to run `react-native-asset`. The docs can be found [here](https://github.com/unimonkiez/react-native-asset).

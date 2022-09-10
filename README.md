[![NPM](https://img.shields.io/npm/v/expo-template-bare-minimum-tvos.svg)](https://www.npmjs.com/package/expo-template-bare-minimum-tvos)

# What
This is a clone of `expo`'s bare minimal template which includes a minimal setup for using unimodules with React Native. Additionally, this template includes `react-native-tvos` support to use with your `expo` based React Native TV projects.

# Why
When you run `expo run:android` command, `expo` checks your project root if `android` folder is there to build your project. If the project doesn't have native code, it runs `prebuild` function to clone and extract the prebuilt project files by using `expo-template-bare-minimum` template. Because the original `expo` template's native `android` project built with the latest `react-native` package, the CLI is going to update your `package.json` file with `react-native@LATEST_VERSION` and put the native project accordingly. THEN YOUR PROJECT WILL BREAK!

# Solution
Use this template as a prebuilt template.

# How
Update your `eas.json` file to modify your `prebuild` command:

```
"prebuildCommand": "prebuild --template https://github.com/abdullahceylan/expo-template-bare-minimum-tvos --no-install"
```

That's all!

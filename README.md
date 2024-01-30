# Antilatency SDK 4.2.1 for Unreal Engine

Git command to clone this subset: `git clone --branch subset-d9e7113cf6b666f441d66e3ccdc223eb2a513b0e --single-branch https://github.com/AntilatencySDK/Release_4.2.1.git AntilatencySDK`

## Content description

This is a subset of Antilatency SDK release 4.2.1. You can find all its settings using this [link](https://developers.antilatency.com/Sdk/Configurator_en.html#{"Libraries":{"AltEnvironmentAdditionalMarkers":true,"AltEnvironmentArbitrary2D":true,"AltEnvironmentHorizontalGrid":true,"AltEnvironmentPillars":true,"AltEnvironmentSelector":true,"AltTracking":true,"Bracer":true,"DeviceNetwork":true,"HardwareExtensionInterface":true,"IllumetryDisplay":false,"RadioMetrics":true,"StereoGlasses":false,"StorageClient":true,"TrackingAlignment":true},"OS":{"Android":{"aar":true},"WindowsDesktop":{"x64":true}},"Release":"4.2.1","Target":"UnrealEngine","TargetSettings":{"MathTypes":"Default","UnrealEngineBlueprintsSamples":true,"UnrealEngineVersion":5.1}}). If you need to add or remove some feature to this subset, you can use the link above to make another subset that will match your requirements.

## Installation guide

There are 2 ways of installing the plugin to Unreal Engine:

- as a project plugin
- as an engine plugin

In the first case this plugin will be available only in the project where it is installed, in the second - in every project.

### Installing the plugin

This plugin is supplied with source code only, so it should be compiled before using. If you plan to use this plugin as a project plugin and your project is configured as a source project, you can skip this part and just copy it to the `Plugins` folder as described in [this section](#installing-as-project-plugin).

#### Building the plugin

- create a new source project using the engine version you need
- create a `Plugins` directory in the project root directory
- create an `AntilatencySDK` directory in the `Plugins` directory
- copy plugin content to the `AntilatencySDK` directory
- open this project in Unreal Engine

If you are going to use this plugin as a project plugin, you can freely stop here and copy/paste the entire 'AntilatencySDK' directory into the `Plugins` directory of your project.

If you are going to use this plugin as an engine plugin, continue this steps:

- open `Plugins` window using the `Edit/Plugins` menu item
- find and select the Antilatency SDK plugin
- click on the `Package...` link
- select the directory where the compiled plugin will be placed, and press `Select Folder`
- wait for the end of the build progress

Pay attension that if you copy the packaged plugin to the `Plugins` directory of the project, the plugin may be incorrectly packaged with your game because of missing `"EnabledByDefault": false` line in the `AntilatencySDK.uplugin`. This behaviour takes place in Unreal Engine 4.25.x - 4.26.x.

#### Installing as project plugin

Place the plugin to the `<path_to_your_project>/Plugins` directory, so the path to the AntilatencySDK.uplugin will be `<path_to_your_project>/Plugins/AntilatencySDK/AntilatencySDK.uplugin`

#### Installing as engine plugin

Place the packaged plugin to the `<path_to_unreal_engine_istallation_dir>/Engine/Plugins/Runtime` directory, so the path to the AntilatencySDK.uplugin will be `<path_to_unreal_engine_istallation_dir>/Engine/Plugins/Runtime/AntilatencySDK/AntilatencySDK.uplugin`

# TERAFORM Project Structure

This document outlines the initial folder and file structure of the **TERAFORM** project. The project is a standard Flutter application.

## Directory Structure

Here is a breakdown of the key directories and files in the project:

### Root Directory: `d:\TERAFORM\TERAFORM\teraform`

*   **`.dart_tool/`**: Used by Dart tools (like Pub) to store state and generated files. You generally don't need to commit this to version control.
*   **`.idea/`**: Contains project-specific settings for JetBrains IDEs (like Android Studio or IntelliJ IDEA).
*   **`android/`**: Contains the Android-specific code and configuration required to build the Flutter app for Android devices.
*   **`ios/`**: Contains the iOS-specific code and configuration required to build the Flutter app for Apple devices.
*   **`lib/`**: **This is the most important directory.** It contains all the Dart code for your Flutter application.
    *   `main.dart`: The main entry point of the Flutter application.
    *   `core/`: Core configuration, networking, database, and location logic.
    *   `features/`: Modular features (auth, home, walk, territory, leaderboard, missions, profile, settings).
    *   `shared/`: Shared UI components, widgets, and themes.
*   **`linux/`**: Contains the Linux-specific code and configuration.
*   **`macos/`**: Contains the macOS-specific code and configuration.
*   **`test/`**: Contains unit and widget tests for your application.
*   **`web/`**: Contains the web-specific code and configuration (like `index.html`).
*   **`windows/`**: Contains the Windows-specific code and configuration.

### Key Files in Root

*   **`.gitignore`**: Specifies intentionally untracked files that Git should ignore (e.g., build artifacts, IDE settings).
*   **`README.md`**: The main documentation file for the repository. A good place to describe what the project does and how to run it.
*   **`analysis_options.yaml`**: Configures the lint rules for the Dart analyzer. It helps maintain code quality and consistency.
*   **`pubspec.yaml`**: The most crucial configuration file for a Flutter project. It defines the project's dependencies (packages, assets like images and fonts), version number, and other metadata.
*   **`pubspec.lock`**: Generated automatically based on `pubspec.yaml`. It locks the versions of all dependencies (and transitive dependencies) to ensure consistent builds across different environments.
*   **`teraform.iml`**: An IntelliJ IDEA module file, used by the IDE to keep track of the module's configuration.

## Next Steps

Since this is the beginning of the project, all your custom application code will go into the `lib/` directory. You will likely start by modifying `lib/main.dart` and creating new folders inside `lib/` (like `screens`, `models`, `widgets`, etc.) to organize your code as the project grows.


## Detailed Project Tree

```text
Folder PATH listing for volume New Volume
Volume serial number is C6BD-4A83
D:.
|   .gitignore
|   .metadata
|   analysis_options.yaml
|   pubspec.lock
|   pubspec.yaml
|   README.md
|   start.md
|   teraform.iml
|   tree_output_cmd.txt
|   
+---.dart_tool
|   |   package_config.json
|   |   package_graph.json
|   |   version
|   |   
|   \---dartpad
|           web_plugin_registrant.dart
|           
+---.idea
|   |   modules.xml
|   |   workspace.xml
|   |   
|   +---libraries
|   |       Dart_SDK.xml
|   |       KotlinJavaRuntime.xml
|   |       
|   \---runConfigurations
|           main_dart.xml
|           
+---android
|   |   .gitignore
|   |   build.gradle.kts
|   |   gradle.properties
|   |   gradlew
|   |   gradlew.bat
|   |   local.properties
|   |   settings.gradle.kts
|   |   teraform_android.iml
|   |   
|   +---.gradle
|   |   +---8.14
|   |   |   |   gc.properties
|   |   |   |   
|   |   |   +---checksums
|   |   |   |       checksums.lock
|   |   |   |       
|   |   |   +---expanded
|   |   |   +---fileChanges
|   |   |   |       last-build.bin
|   |   |   |       
|   |   |   +---fileHashes
|   |   |   |       fileHashes.bin
|   |   |   |       fileHashes.lock
|   |   |   |       
|   |   |   \---vcsMetadata
|   |   +---buildOutputCleanup
|   |   |       buildOutputCleanup.lock
|   |   |       cache.properties
|   |   |       
|   |   \---vcs-1
|   |           gc.properties
|   |           
|   +---app
|   |   |   build.gradle.kts
|   |   |   
|   |   \---src
|   |       +---debug
|   |       |       AndroidManifest.xml
|   |       |       
|   |       +---main
|   |       |   |   AndroidManifest.xml
|   |       |   |   
|   |       |   +---java
|   |       |   |   \---io
|   |       |   |       \---flutter
|   |       |   |           \---plugins
|   |       |   |                   GeneratedPluginRegistrant.java
|   |       |   |                   
|   |       |   +---kotlin
|   |       |   |   \---com
|   |       |   |       \---example
|   |       |   |           \---teraform
|   |       |   |                   MainActivity.kt
|   |       |   |                   
|   |       |   \---res
|   |       |       +---drawable
|   |       |       |       launch_background.xml
|   |       |       |       
|   |       |       +---drawable-v21
|   |       |       |       launch_background.xml
|   |       |       |       
|   |       |       +---mipmap-hdpi
|   |       |       |       ic_launcher.png
|   |       |       |       
|   |       |       +---mipmap-mdpi
|   |       |       |       ic_launcher.png
|   |       |       |       
|   |       |       +---mipmap-xhdpi
|   |       |       |       ic_launcher.png
|   |       |       |       
|   |       |       +---mipmap-xxhdpi
|   |       |       |       ic_launcher.png
|   |       |       |       
|   |       |       +---mipmap-xxxhdpi
|   |       |       |       ic_launcher.png
|   |       |       |       
|   |       |       +---values
|   |       |       |       styles.xml
|   |       |       |       
|   |       |       \---values-night
|   |       |               styles.xml
|   |       |               
|   |       \---profile
|   |               AndroidManifest.xml
|   |               
|   \---gradle
|       \---wrapper
|               gradle-wrapper.jar
|               gradle-wrapper.properties
|               
+---ios
|   |   .gitignore
|   |   
|   +---Flutter
|   |   |   AppFrameworkInfo.plist
|   |   |   Debug.xcconfig
|   |   |   flutter_export_environment.sh
|   |   |   Generated.xcconfig
|   |   |   Release.xcconfig
|   |   |   
|   |   \---ephemeral
|   |           flutter_lldbinit
|   |           flutter_lldb_helper.py
|   |           
|   +---Runner
|   |   |   AppDelegate.swift
|   |   |   GeneratedPluginRegistrant.h
|   |   |   GeneratedPluginRegistrant.m
|   |   |   Info.plist
|   |   |   Runner-Bridging-Header.h
|   |   |   SceneDelegate.swift
|   |   |   
|   |   +---Assets.xcassets
|   |   |   +---AppIcon.appiconset
|   |   |   |       Contents.json
|   |   |   |       Icon-App-1024x1024@1x.png
|   |   |   |       Icon-App-20x20@1x.png
|   |   |   |       Icon-App-20x20@2x.png
|   |   |   |       Icon-App-20x20@3x.png
|   |   |   |       Icon-App-29x29@1x.png
|   |   |   |       Icon-App-29x29@2x.png
|   |   |   |       Icon-App-29x29@3x.png
|   |   |   |       Icon-App-40x40@1x.png
|   |   |   |       Icon-App-40x40@2x.png
|   |   |   |       Icon-App-40x40@3x.png
|   |   |   |       Icon-App-60x60@2x.png
|   |   |   |       Icon-App-60x60@3x.png
|   |   |   |       Icon-App-76x76@1x.png
|   |   |   |       Icon-App-76x76@2x.png
|   |   |   |       Icon-App-83.5x83.5@2x.png
|   |   |   |       
|   |   |   \---LaunchImage.imageset
|   |   |           Contents.json
|   |   |           LaunchImage.png
|   |   |           LaunchImage@2x.png
|   |   |           LaunchImage@3x.png
|   |   |           README.md
|   |   |           
|   |   \---Base.lproj
|   |           LaunchScreen.storyboard
|   |           Main.storyboard
|   |           
|   +---Runner.xcodeproj
|   |   |   project.pbxproj
|   |   |   
|   |   +---project.xcworkspace
|   |   |   |   contents.xcworkspacedata
|   |   |   |   
|   |   |   \---xcshareddata
|   |   |           IDEWorkspaceChecks.plist
|   |   |           WorkspaceSettings.xcsettings
|   |   |           
|   |   \---xcshareddata
|   |       \---xcschemes
|   |               Runner.xcscheme
|   |               
|   +---Runner.xcworkspace
|   |   |   contents.xcworkspacedata
|   |   |   
|   |   \---xcshareddata
|   |           IDEWorkspaceChecks.plist
|   |           WorkspaceSettings.xcsettings
|   |           
|   \---RunnerTests
|           RunnerTests.swift
|           
+---lib
|   |   main.dart
|   |   
|   +---core
|   |   +---config
|   |   +---database
|   |   +---location
|   |   \---network
|   +---features
|   |   +---auth
|   |   +---home
|   |   +---leaderboard
|   |   +---missions
|   |   +---profile
|   |   +---settings
|   |   +---territory
|   |   \---walk
|   \---shared
|       +---theme
|       \---widgets
+---linux
|   |   .gitignore
|   |   CMakeLists.txt
|   |   
|   +---flutter
|   |       CMakeLists.txt
|   |       generated_plugins.cmake
|   |       generated_plugin_registrant.cc
|   |       generated_plugin_registrant.h
|   |       
|   \---runner
|           CMakeLists.txt
|           main.cc
|           my_application.cc
|           my_application.h
|           
+---macos
|   |   .gitignore
|   |   
|   +---Flutter
|   |   |   Flutter-Debug.xcconfig
|   |   |   Flutter-Release.xcconfig
|   |   |   GeneratedPluginRegistrant.swift
|   |   |   
|   |   \---ephemeral
|   |           Flutter-Generated.xcconfig
|   |           flutter_export_environment.sh
|   |           
|   +---Runner
|   |   |   AppDelegate.swift
|   |   |   DebugProfile.entitlements
|   |   |   Info.plist
|   |   |   MainFlutterWindow.swift
|   |   |   Release.entitlements
|   |   |   
|   |   +---Assets.xcassets
|   |   |   \---AppIcon.appiconset
|   |   |           app_icon_1024.png
|   |   |           app_icon_128.png
|   |   |           app_icon_16.png
|   |   |           app_icon_256.png
|   |   |           app_icon_32.png
|   |   |           app_icon_512.png
|   |   |           app_icon_64.png
|   |   |           Contents.json
|   |   |           
|   |   +---Base.lproj
|   |   |       MainMenu.xib
|   |   |       
|   |   \---Configs
|   |           AppInfo.xcconfig
|   |           Debug.xcconfig
|   |           Release.xcconfig
|   |           Warnings.xcconfig
|   |           
|   +---Runner.xcodeproj
|   |   |   project.pbxproj
|   |   |   
|   |   +---project.xcworkspace
|   |   |   \---xcshareddata
|   |   |           IDEWorkspaceChecks.plist
|   |   |           
|   |   \---xcshareddata
|   |       \---xcschemes
|   |               Runner.xcscheme
|   |               
|   +---Runner.xcworkspace
|   |   |   contents.xcworkspacedata
|   |   |   
|   |   \---xcshareddata
|   |           IDEWorkspaceChecks.plist
|   |           
|   \---RunnerTests
|           RunnerTests.swift
|           
+---test
|       widget_test.dart
|       
+---web
|   |   favicon.png
|   |   index.html
|   |   manifest.json
|   |   
|   \---icons
|           Icon-192.png
|           Icon-512.png
|           Icon-maskable-192.png
|           Icon-maskable-512.png
|           
\---windows
    |   .gitignore
    |   CMakeLists.txt
    |   
    +---flutter
    |       CMakeLists.txt
    |       generated_plugins.cmake
    |       generated_plugin_registrant.cc
    |       generated_plugin_registrant.h
    |       
    \---runner
        |   CMakeLists.txt
        |   flutter_window.cpp
        |   flutter_window.h
        |   main.cpp
        |   resource.h
        |   runner.exe.manifest
        |   Runner.rc
        |   utils.cpp
        |   utils.h
        |   win32_window.cpp
        |   win32_window.h
        |   
        \---resources
                app_icon.ico
                
```


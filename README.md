# Expo CLI Android Build Failure: Gradle Dependency Resolution

This repository demonstrates a bug where the Expo CLI fails to build an Android APK due to issues resolving Gradle dependencies.  Even with seemingly correct configuration, the build process may fail with vague error messages. This often requires manual intervention and troubleshooting.

## Bug Description
The Expo CLI's Android build process fails.  The error messages from Gradle are often unhelpful, providing little indication of the root cause.  This issue may persist even after carefully reviewing the project's `build.gradle` files.

## Reproduction Steps
1. Clone this repository.
2. Navigate to the project directory.
3. Attempt to build an Android APK using `expo build:android`.
4. Observe the build failure and the associated error messages.

## Solution
The solution typically involves manual investigation of Gradle's dependency resolution process, potentially including:
* Checking network connectivity and Gradle's repository access.
* Cleaning the project's build cache (`./gradlew clean`).
* Investigating specific dependencies and their versions, ensuring consistency.
* Manually adding missing or updating conflicting dependencies in `build.gradle` files. 
* Using a newer version of Expo CLI and its associated dependencies.
* Using a different Android build system such as using Android studio.
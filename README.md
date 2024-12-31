# Expo ImagePicker Inconsistent URI Return Bug

This repository demonstrates a bug in Expo's ImagePicker library where the `launchImageLibraryAsync` function sometimes returns a promise that resolves with an object lacking a `uri` property, even after the user successfully selects an image. The problem is inconsistent; sometimes it works, and sometimes it doesn't, making debugging difficult. 

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on a physical device or emulator.
4. Try to select an image from your gallery multiple times.
5. Observe that on some attempts, the `uri` field of the returned object is empty, preventing the use of the selected image.
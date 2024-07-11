# Release notes

## Version 1.0.0:
  - Open photo library is now supported on Android
  - Open photo library is now supported on iOS

# Usage

APIs provided by EnviPicker:

- `EnviPicker.Instance.OpenPhotoLibrary(result => {})`: Open photo library from device.

```C#
EnviPicker.Instance.OpenPhotoLibrary(result =>
{
  result.Match(
    value =>
    {
      // Handle value here
    },
    error =>
    {
      // Handle error here
    }
  );
});
// output:
// {
//   "error": "",
//   "value": {
//     "uri": "path",
//     "data": "base64"
//   }
// }
```
# Plist entries
In order for your app to access photo libraries, you'll need to add the below plist entry:

- Privacy - Photo Library Usage Description (library)
```Text
<key>NSPhotoLibraryUsageDescription</key>
<string>{your wording}</string>
```

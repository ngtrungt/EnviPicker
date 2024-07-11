# Integration guide

APIs provided by EnviPicker:

- `EnviPicker.Instance.OpenPhotoLibrary(result => {})`: Open photo library from device.

```C#
// Usage
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

Privacy - Photo Library Usage Description (library)
<key>NSPhotoLibraryUsageDescription</key>
<string>{your wording}</string>

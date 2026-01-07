# Raw JSON Files

This directory is designated for storing raw JSON data files for the iOS application.

## Usage

Place your `.json` files in this directory. These files can contain:
- Configuration data
- Mock data for testing
- Static content
- API response examples
- Any other structured data in JSON format

## Example

See `example.json` for a sample JSON file structure.

## Accessing JSON Files in iOS

To access JSON files from this directory in your iOS app:

### Swift
```swift
if let path = Bundle.main.path(forResource: "filename", ofType: "json", inDirectory: "Resources/Data") {
    do {
        let data = try Data(contentsOf: URL(fileURLWithPath: path))
        let json = try JSONSerialization.jsonObject(with: data, options: [])
        // Use your JSON data
    } catch {
        print("Error loading JSON: \(error)")
    }
}
```

### Using Codable
```swift
struct YourModel: Codable {
    // Your properties
}

if let path = Bundle.main.path(forResource: "filename", ofType: "json", inDirectory: "Resources/Data") {
    do {
        let data = try Data(contentsOf: URL(fileURLWithPath: path))
        let decoder = JSONDecoder()
        let model = try decoder.decode(YourModel.self, from: data)
        // Use your decoded model
    } catch {
        print("Error decoding JSON: \(error)")
    }
}
```

## Notes

- Make sure to add these JSON files to your Xcode project as resources
- Ensure files are included in the target's "Copy Bundle Resources" build phase

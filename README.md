# ipa-app-repos

IPA repository with organized resource management.

## Directory Structure

```
ios-app-repos/
├── Resources/
│   └── Data/           # Raw JSON files storage
│       ├── README.md   # Documentation for JSON files
│       └── example.json # Sample JSON file
└── README.md
```

## Raw JSON Files

The `Resources/Data/` directory is dedicated to storing raw JSON data files. This is where you can place:

- Configuration files
- Mock data for testing and development
- Static content data
- API response examples
- Any structured data in JSON format

For detailed information on how to use JSON files in your iOS app, see [Resources/Data/README.md](Resources/Data/README.md).

## Getting Started

1. Place your `.json` files in the `Resources/Data/` directory
2. Add the files to your Xcode project
3. Ensure they are included in your target's "Copy Bundle Resources" build phase
4. Access them using `Bundle.main.path(forResource:ofType:inDirectory:)`

## Example

See `Resources/Data/example.json` for a sample JSON file structure.

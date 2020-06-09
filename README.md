## Building

### Prerqs

1. You must have cocoapods installed to build this repo:

```
sudo gem install cocoapods
```

2. Xcode and Carthage must also be installed and ready to go

### Building a Carthage Archive

Run pod install from the root directoy to download and build the pods:

```
pod install
```

Then build the project with carthage:

```
carthage build --configuration Debug --no-skip-current --platform iOS
zip -vr FlipperKit.framework.zip ./Carthage/ -x "*.DS_Store"
```

## Upload the build

1. Update `carthage.json` with the new build location (if changed)
1. Commit the newly-generated carthage  zip file

## Using 

To use, add this line to your `Cartfile`:

```
binary "https://github.com/jbfitb/FlipperKit/raw/master/carthage.json" == 0.45.0
```
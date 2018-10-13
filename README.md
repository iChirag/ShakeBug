# ShakeBug

Bug &amp; Crash reporting tool.

## Installation

### CocoaPods

To integrate ShakeBug into your Xcode project using [CocoaPods](https://cocoapods.org), specify it in your `Podfile`:

```ruby
pod 'ShakeBug'
```

Then, run the following command:

```bash
$ pod install
```

## Code

1. Import the ShakeBug framework header into your app delegate.

    ```swift
    // Swift
    import ShakeBug
    ```
    
    
    ```objective-c
    // Objective-C
    #import <ShakeBug/ShakeBug.h>
    ```

2. Add the following to your app delegate's `application:didFinishLaunchingWithOptions:` method.
	
   ```swift
   // Swift
   ShakeBug.sharedInstance().initiate(withKey: “<Your Key>")
   ```
    
   ```objective-c
   // Objective-C
   [[ShakeBug sharedInstance] initiateWithKey:@"<Your Key>"];
   ```

	Be sure to replace `<Your Key>` with your application key which given by ShakeBug website..
	

## Optional Settings

1. Add the following to your app delegate's `application:didFinishLaunchingWithOptions:` method for showing or not showing first time tutorial screen

   ```objective-c
   // Objective-C
   [[ShakeBug sharedInstance] showTutorialScreenFirstTime:NO];// OR pass YES to show Tutorial screen
   ```

2. If you dont want to show bug or crash from Simulator then use following code `application:didFinishLaunchingWithOptions:`

   ```objective-c
   // Objective-C
       [[ShakeBug sharedInstance] allowBugCrashFromSimulator:YES];// OR pass NO if you dont want to show bug from Simulator
   ```

	
## Usage

Build & run your app. Once your app is running, shake your device (\^⌘Z in the simulator) to report a bug! Bug reports are sent directly to your email address.


## Contact

Contact us on softnoesis@gmail.com in case of any use.

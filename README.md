# WatchApp-Sample-App
in this Sample Watch kit App synchronizes data between Watch app and containing Parent iPhone app (Objective-C) 
App Groups is used to share Data between Parent App and the Watch App Extension.

eg:


	

First, you have to enable app groups for your target:

enter image description here

Then you can start to write and read objects via NSUserDefaults:

// write 
let sharedDefaults = NSUserDefaults(suiteName: appGroupName)
sharedDefaults?.setInteger(1, forKey: "myIntKey")


// read
let sharedDefaults = NSUserDefaults(suiteName: appGroupName)
let myIntValue = sharedDefaults?.integerForKey("myIntKey")

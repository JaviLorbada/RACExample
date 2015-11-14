Steps to reproduce error:

1. Clone repo `git clone https://github.com/jakecraige/RACExample.git`
1. Run this command to verify the framework branch exists,
   `git checkout origin/framework && git checkout -b framework && git checkout example-app`
1. Update `Cartfile` to the path where you cloned this repo
1. Run `carthage update --platform iOS`.
   If you see a "code sign is required" error, try running again.

Error output I received:

```
RACExample[example-app] $ carthage update --platform iOS
*** Fetching RACExample
*** Fetching ReactiveCocoa
*** Fetching Result
*** Checking out RACExample at "3acc6eb4987fadc17042d29e9c0fe7e967e8b222"
*** Checking out Result at "0.6.0-beta.5"
*** Downloading ReactiveCocoa.framework binary at "v4.0-alpha.3"
*** xcodebuild output can be found in /var/folders/vb/jz3wqx8153vcdhm6dqmd99d80000gn/T/carthage-xcodebuild.OwMhNq.log
*** Building scheme "Result-iOS" in Result.xcodeproj
*** Building scheme "RGB" in RGB.xcworkspace
** BUILD FAILED **


The following build commands failed:
        CompileSwift normal x86_64
        CompileSwiftSources normal x86_64 com.apple.xcode.tools.swift.compiler
(2 failures)
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:67:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:68:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:69:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:70:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:71:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:72:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:73:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:74:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:75:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:76:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:77:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:78:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:79:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:80:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:81:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:82:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:83:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:84:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
/tmp/RACExample/Carthage/Checkouts/RACExample/Carthage/Checkouts/ReactiveCocoa/ReactiveCocoa/ReactiveCocoa.h:85:10: error: include of non-modular header inside framework module 'ReactiveCocoa'
<unknown>:0: error: too many errors emitted, stopping now
<unknown>:0: error: could not build Objective-C module 'ReactiveCocoa'
A shell task failed with exit code 65:
** BUILD FAILED **


The following build commands failed:
        CompileSwift normal x86_64
        CompileSwiftSources normal x86_64 com.apple.xcode.tools.swift.compiler
(2 failures)
```

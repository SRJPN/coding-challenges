# Compatible Version Groups

In Android (the popular Google mobile operating system), the executable files storing apps on devices are called "APKs".
And each APK contains something called a "Manifest" which stores which devices it is compatible with.
So for example, it might say needs a specific Android version, or needs a GPS chip. In this question, we are only going to think about the Android version requirements in the Manifest.

There are two values minSDKVersion and maxSDKVersion. Each of these is optional, and inclusive.
By this I mean APKs don't have to specify minSDKVersion, but if they specify minSDKVersion = 3, then Android versions 3,4,5,etc all match, but 1 and 2 don't.

An app developer can upload multiple APKs for their app to the Play Store, each with a different manifest. For example, they might have three APKs:

APK	Min SDK Version	Max SDK Version
APK A	4	-
APK B	-	16
APK C	7	10
Now, on Google Play you can have more than one APK per App, and we need to decide which one to deliver.
So you could have A,B, and C. As part of this process we need to split up the space of all phones to which APKs they match.

We want to divide the integer list of SDK versions into intervals that match the same APKs. So for this set we want to produce:

(<=3), (4-6), (7-10), (11-16), (>=17)

This is because <=3 matches only, APK B, then (4-6) matches APK A & B, but not C, etc.

Use whatever sensible data structure you want to represent the input and the output.


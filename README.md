ApplicationDelegate.shared.application(
                    application,
                    didFinishLaunchingWithOptions: launchOptions
                )
Settings.isAutoLogAppEventsEnabled = true
Settings.isAdvertiserIDCollectionEnabled = false
Settings.setAdvertiserTrackingEnabled(false)

info.plist

<key>FacebookAdvertiserIDCollectionEnabled</key>
<false/>
<key>FacebookAppID</key>
<string>---</string>
<key>FacebookAutoLogAppEventsEnabled</key>
<true/>
<key>FacebookClientToken</key>
<string>---</string>
<key>FacebookDisplayName</key>
<string>---</string>

Code samples & details

// INSERT YOUR CODE HERE
var example = "Example code"

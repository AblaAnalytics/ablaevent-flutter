# Setup Flutter

## Install

````
abalevent_flutter: # insert version number

````

## Android Setup

Add these values in AndroidManifest.xml

````
<application>
	<activity>
		[...]
	</activity>
	<meta-data android:name="com.posthog.posthog.API_KEY" android:value="phc_ySCF4YinUf6DxprJ5B0jXtzgijeTqFkWPsIIfC3yTrC" />
	<meta-data android:name="com.posthog.posthog.POSTHOG_HOST" android:value="https://eu.posthog.com" />
	<meta-data android:name="com.posthog.posthog.TRACK_APPLICATION_LIFECYCLE_EVENTS" android:value="false" />
	<meta-data android:name="com.posthog.posthog.DEBUG" android:value="false" />
</application>

````
   
## iOS Setup

Add these values in Info.plist

````
<dict>
	[...]
	<key>com.posthog.posthog.API_KEY</key>
	<string>phc_ySCF4YinUf6DxprJ5B0jXtzgijeTqFkWPsIIfC3yTrC</string>
	<key>com.posthog.posthog.POSTHOG_HOST</key>
	<string>https://e.abla.io</string>
	<key>com.posthog.posthog.TRACK_APPLICATION_LIFECYCLE_EVENTS</key>
	<false/>
	[...]
</dict>

````
    
## Send an Event

````
import 'package:abalevent_flutter/posthog_flutter.dart';

Posthog().screen(
	screenName: 'Example Screen',
);

````

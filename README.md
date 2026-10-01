# IML-Texting-App
A simple text messaging app that allows you to group incoming text messages with a label so that the user can tell what the number is for at a glance without saving it as a contact in the phone.

## Features

- **Label grouping** — map one or more phone numbers to a display name.
  Labels are read-only and purely organizational: they are never a send target,
  and the wrapped numbers never know they are grouped.
- **Individual threads** — send and receive with a single number as usual.
- **Group threads** — real multi-recipient MMS conversations stay sendable.
- **Label-titled notifications** — incoming messages are announced under the
  label name.

## Status

Early scaffold. SMS send/receive and label notifications are wired; MMS
handling is in progress.

## Tech

Kotlin, Gradle, AGP 8.5.x, minSdk 26, targetSdk 34, Hilt, Room, ViewBinding.

## Build
```
./gradlew :app:assembleDebug
```
Requires Android SDK 34 and JDK 17.

## Note on the default SMS role

Because Android routes `SMS_DELIVER` and the SMS/MMS provider to a single
default app, this app requests the default-SMS role in order to send and
receive in one place.

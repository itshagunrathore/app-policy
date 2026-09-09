# Privacy Policy for Unpile

**Last updated: 27 August 2026**

Unpile is an Android app that helps you review your own photo library and reclaim storage space.
This policy explains what the app does and does not do with your information.

The short version: **Unpile collects nothing, sends nothing, and has no network access.**

## Information we collect

None.

Unpile does not collect, transmit, or store any personal information. Specifically, it does not
collect:

- Your name, email address, phone number, or any account information — the app has no accounts and no
  sign-in
- Your photos or any part of their content
- Device identifiers, advertising IDs, or location
- Usage analytics, telemetry, or crash reports
- Contacts, calendar, microphone, or camera data

## Network access

Unpile does not request the `INTERNET` permission. The app is technically incapable of making a
network request. You can verify this yourself by inspecting the app's declared permissions in Android's
Settings, or in the `AndroidManifest.xml` file of the published package.

There are no third-party SDKs in the app: no analytics library, no crash reporting service, no advertising
network, no social login.

## Data stored on your device

To function, Unpile keeps two small pieces of information in its own private app storage:

1. **A record of your decisions.** For each photo you review, the app stores the photo's MediaStore ID,
   whether you chose to keep or delete it, the timestamp, the file size, and whether a deletion has been
   carried out by the operating system. This is what stops the app showing you the same photo twice. It
   contains no image data and no file contents.
2. **Your preferences.** Sort order, theme, whether haptics are enabled, and similar settings.

Both live in the app's private directory, which other apps cannot read. Neither is ever sent to us — we
operate no server and the app cannot make a network request.

**Android backup.** Android's own backup system, tied to your Google account rather than to us, is
configured as follows:

- **Your preferences are included.** If you have Android backup enabled, your sort order and theme travel
  to a new device with the rest of your settings. We never see them.
- **Your decision history is excluded**, on purpose. Those records are keyed by device-local photo IDs,
  which a different device assigns to different photos. Restoring them elsewhere would mark unrelated
  photos as already reviewed and hide them from you, so the app opts that database out of both cloud
  backup and direct device transfer.

Uninstalling Unpile deletes both stores from your device. A preferences copy already held in your
own Google account backup is governed by Google's retention, not by us, and is removed by Android when
that backup expires or when you delete it from your account. You can clear the decision history at any
time with **Clear review history** on the app's home screen.

## Permissions and why they are needed

| Permission | Purpose |
| --- | --- |
| Photos and videos (`READ_MEDIA_IMAGES`) | To show you photos from your library so you can review them |
| Selected photos only (`READ_MEDIA_VISUAL_USER_SELECTED`) | To work correctly when you grant access to only some photos on Android 14 and later |
| Read storage (`READ_EXTERNAL_STORAGE`) | The same purpose, on Android 11 and 12 |

Every permission listed is **read-only**. Unpile holds no permission to write to or modify your
photos — when you choose to delete one, the app asks Android to move it to the trash, and Android does
the moving.

Unpile does **not** request "All files access" (`MANAGE_EXTERNAL_STORAGE`), which would grant access
to every file on your device. It is not needed and is not used.

Photo access is used solely to display photos for your review and to ask the operating system to move the
ones you choose to the system trash. Photos are never copied, uploaded, or transmitted anywhere.

## How deletion works

When you mark a photo for deletion, nothing happens to the file. Unpile records your choice and waits.

When you tap **Move to trash**, the app asks Android to move that batch of files to the **system trash**,
and Android shows you its own confirmation dialog. Only after the operating system confirms does Unpile
record the deletion as done.

Photos in the system trash remain recoverable through your gallery app, typically for 30 days, according to
your device's own policy. Unpile has no ability to permanently delete a photo, and no ability to
restore one from the trash — both of those are handled by Android and your gallery app.

## Children's privacy

Unpile does not collect any information from anyone, including children under 13. It contains no ads,
no in-app purchases, and no external links.

## Changes to this policy

If this policy changes, the updated version will be posted at this URL with a new "Last updated" date. If a
future version of the app were ever to collect data, that would be disclosed here and in the app's Google
Play Data safety section before the change took effect.

## Contact

Questions about this policy or the app:

**needcode.web@gmail.com**

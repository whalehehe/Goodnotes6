# Goodnotes Local — v12

A modified Goodnotes 7.1.28 IPA focused on local document use, optional guest access, and cloud-provider backup.

**Status: experimental. Static checks passed; v12 has not been tested on the iPad.**

## Features

- Changes normal account/settings subscription labels to **◇ Pro**. This is cosmetic.
- Enables the native guest-mode feature, subject to the app's existing account and organization checks.
- Changes local permission checks to allow document creation, editing, imports, watermark-free export, larger imports, and longer recording.
- Retains the local document-count change that selects the existing maximum-count path.
- Hides the main iCloud/Goodnotes Cloud settings section and suppresses three cloud-enrollment startup tasks.
- Keeps Manual Backup and exposes native Automatic Backup controls for Google Drive/OneDrive.

## Benefits

- Focuses on local use without requiring a new Goodnotes account where native guest mode is available.
- Removes specific local restrictions and reduces exposure to the cloud paths implicated in earlier crashes.
- Preserves the existing provider sign-in and backup implementation.
- Leaves the PDF rendering-memory budget unchanged.

## Limitations

- **Not a real Pro subscription.** The badge does not grant server entitlements, AI credits, collaboration, or Goodnotes Cloud access.
- Google Drive/OneDrive require their own sign-in and internet connection. Uploads remain untested.
- Auto Backup uploads copies **one way**; it does not sync cloud edits back into Goodnotes.
- Existing accounts and credentials remain intact. Guest access and zero Goodnotes authentication traffic are not guaranteed.
- Other cloud controls/callers may remain. Crash-free operation is not established.
- The reported DOCX import/CSV-parser error remains unresolved.
- More than 1,000 documents, reliable editing/reopening, and the new badge's appearance remain unverified.

## Install and test

1. Keep a verified, editable document backup.
2. Re-sign the [v12 IPA](Goodnotes-7.1.28-offline-v12-RESIGN-REQUIRED.ipa) and its nested components in eSign with your certificate/profile.
3. Use the native skip-sign-in option if available; existing signed-in state is not automatically converted to guest mode.
4. Import a small PDF, edit it, close/reopen the app, and confirm the edit persists.
5. Test one Google Drive/OneDrive backup and verify the uploaded file before increasing your library size.

See [technical notes](offline-v12-notes.md) and the [patch manifest](offline-v12-patch-manifest.json) for exact changes and verification details.

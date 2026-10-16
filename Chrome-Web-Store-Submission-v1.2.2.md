# Chrome Web Store submission — Business Suite 1.2.2

Upload `Business-Suite-Chrome-Extension.zip` without extracting it.

## Single purpose

Business Suite is an offline-first business operations workspace for planning, customers, sales, payments, tasks, work tracking, notes, exports, reminders and optional user-owned Google Drive backup/sync.

## Privacy policy

Use this public URL:

`https://keralawebsitedesign.com/privacy.html`

Publish the matching `website/privacy.html` file on that URL before submitting the extension.

## Permission justifications

Paste these explanations into the Privacy practices form when Chrome asks for them:

- `storage`: Stores the user's business records, settings, licence lease and sync state locally so the business workspace works offline.
- `unlimitedStorage`: Business records, document attachments and backup history can exceed Chrome's small default extension storage quota.
- `downloads`: Saves a PDF, CSV or user-requested backup to the user's Downloads folder only after an export action.
- `identity`: Starts the user-initiated Google OAuth flow for optional Google Drive sync. The extension never receives the user's Google password.
- `alarms`: Runs due-item reminders, licence refresh checks and user-enabled daily-summary preparation at the selected time.
- `notifications`: Shows user-enabled reminders for due payments, tasks, follow-ups and appointments.
- `https://license.keralawebsitedesign.com/*`: Activates and verifies trials/licences and opens the selected subscription payment flow.
- `https://oauth2.googleapis.com/*`: Exchanges and refreshes Google OAuth tokens for the optional Drive connection.
- `https://www.googleapis.com/*`: Creates and updates only the Business Suite files/folder authorised under the `drive.file` scope.
- `https://web.whatsapp.com/*`: Places user-selected reminder text or an invoice PDF into WhatsApp Web. The user reviews the content and presses Send; the extension does not auto-send.

## Data-use disclosures

Declare the following categories because the extension handles them:

- Personally identifiable information: name, email address and phone number entered for licensing or stored by the user in business/customer records.
- Financial and payment information: business sales, billing, expense and payment records entered by the user. Payment-card details are handled by the external payment provider and are not received by the extension.
- Authentication information: Google OAuth access/refresh tokens used for optional Drive sync. Google passwords are never received.
- Website content: on WhatsApp Web, the extension inserts only the text/PDF the user asked it to prepare; it does not collect chat history.
- User activity: record counts and total local-storage bytes are sent to the licence service with licence-status requests.
- Device information: an anonymous installation identifier and device/platform label are used for trials and licensed-device limits.

The data is used for the extension's visible features, licence/security controls, fraud prevention and support. It is not sold, used for advertising, used for credit decisions, or transferred for unrelated purposes.

Certify that the use of Google user data complies with the Google API Services User Data Policy, including Limited Use.

## Store listing and reviewer note

Suggested reviewer note:

> Business Suite works locally after licence verification. Google Drive sync is optional and user initiated. The extension requests `drive.file`, creates/uses the visible `Business Suite` folder and does not request access to unrelated Drive files. WhatsApp Web support only prepares user-selected text or a PDF; the user must review it and press Send. All executable code is packaged in this Manifest V3 ZIP.

The listing description and screenshots must describe the same behavior. Do not claim that WhatsApp messages are sent automatically.

## Google OAuth after Web Store publication

The installed Web Store extension ID must match the OAuth redirect URI. In Google Cloud, keep the final redirect URI:

`https://<FINAL_EXTENSION_ID>.chromiumapp.org/google`

If the Store assigns a different extension ID from the development build, update the OAuth client before testing Drive sign-in.

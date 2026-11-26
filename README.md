# Prakshal DigiBulk
Windows desktop bulk sender for Prakshal IT Academy Gandhinagar. Electron and Node.js; local JSON data, Excel/CSV import and export, official Meta Cloud API.

## Start
Install Node.js 22+, then run:
```bash
npm install
npm test
npm start
```
On Windows run `npm run build` to build an NSIS installer.

## Use
1. In Meta Business Platform create an approved marketing template and configure a phone number ID and access token. Enter a supported Graph API version in Settings and test the connection.
2. Import opted-in contacts using the sample CSV columns (mobile,name,consent). Consent must be yes. Use text format for phone numbers. Manual contacts require opt-in too.
3. Choose the template name and language. Enter positional body variables in order, one per line; {name} inserts the imported name. Attach supported image, PDF, Office document or MP4 only if the approved template has the matching media header.
4. Test with a single consenting recipient, then review and submit your campaign. Stop cancels subsequent requests, not a request already in flight.
5. Check submission history, export Excel, and enter unsubscribed numbers in the opt-out list.

## Limitations
API usage charges and template rules apply. No unofficial WhatsApp Web automation, QR login, or unlimited free messaging. Accepted means API submission, not delivered/read. Delivery webhooks and automatic opt-out synchronization are not implemented; opt-outs must be recorded manually. Failed/unknown submissions stop the campaign; inspect Meta records before retrying. The preview shows variables, not the actual approved template wording. Data is stored on the local machine; credentials use Electron safeStorage. Protect the PC and never commit real contacts, reports or secrets. Live API, Windows packaging and runtime have not been tested by the author. Unit tests cover contact validation only.

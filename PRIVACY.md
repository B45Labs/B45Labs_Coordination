# B45 Labs: Privacy Policy


**Effective date:** 2026-01-01  
**Last updated:** 2026-11-15  
**Applies to:** B45 Labs | Coordination 3.0.0, B45 Labs | Library 2.0.0, B45 Labs | Connect 0.0.1, B45 Labs | Wayfinder 0.0.1 (together, the "Software") and the website b45labs.com (the "Website").

## 1. Who we are and how to reach us

B45 Labs ("B45 Labs", "we", "our", "us") makes tools for Autodesk Revit and Autodesk Navisworks.
For privacy questions or requests, write to **support@b45labs.com**.

## 2. In short

- Usage reporting is **on by default** and one switch turns it off. It sends counts tied to a random install ID, error reports, one installation record and a coarse location (continent, country and state or province, never a city).
- We never collect your model, its geometry, file names or paths, or your Windows user name.
- Your profile (name, e-mail, company, role) leaves your computer **only if you turn on "Also sync my profile"**. It is off by default.
- Update checks and notices are **not** behind the usage switch. A version can be locked remotely until you update.
- Connect sends your prompts and the model data its tools read to the AI provider **you** choose. We do not receive them.
- We keep data for **up to 36 months** and delete it earlier when you ask.
- We may publish **aggregated, de-identified statistics**, including on our website and in research. Nothing in them identifies you or your organization.

## 3. What the Software collects

Collection works in **two tiers**:

- **Essential data** (3.1 to 3.5) is collected by default to operate, support and improve the Software, on the basis of our legitimate interest in running and improving a product. The switch **"Share usage data"**, in My Profile, controls it for all four products: Connect has no switch of its own and reads the one in Coordination; Wayfinder has its own My Profile and shares the same setting with the other products on the computer.
- **Optional data** (3.6 and 3.7) is sent only if you opt in or do something yourself.

### 3.1 Usage data
The name of each command or button you use, how many times, whether it worked, and when. The Software version and build, the Revit or Navisworks name, version and build, and the interface language. Connect also counts what was used (pane opened, a message sent, a tool run, which kind of external AI client connected), never the content.

### 3.2 Error and diagnostic data
When a B45 Labs command fails, an error report is sent with the command that was active.
- **Coordination and Library:** the report carries Revit's error message and stack trace. File paths, Revit file names and e-mail addresses are removed before it leaves your computer. Revit can name an element, view or family in that message, and we cannot remove those names automatically.
- **Connect:** the report carries only the exception type and its code, never a message.
- **Wayfinder:** for an error it handled, the exception type and its code (plus the type of an inner exception and how many times it happened); for a crash, a short message and a stack trace with file paths, model file names and e-mail addresses removed.
Errors of other add-ins are not reported.

### 3.3 Installation and update data
When the Software first runs and when its version or language changes: the version first installed, the running version, the version it was upgraded from, and the dates it was first seen and last updated.

### 3.4 Identifiers
A random installation identifier (`install_id`) shared by the B45 Labs products on the same computer, and a random session identifier created each time the host program starts. They contain no name or e-mail. They are used to group usage and error records and, only if you sync your profile or send feedback, to link that profile or message to your installation.

### 3.5 Location
Continent, country and state or province, taken from your IP address when the installation record is sent. We never collect a city, a street address or GPS coordinates. The lookup is made from your computer to **ipwhois.app**, a public IP-lookup service, which sees your IP address as any website you visit does. B45 Labs keeps only the three fields it returns and does not read or save your IP address in its data. Our hosting provider receives your IP address with each request and may keep technical logs (see section 9). Turning off the usage switch stops the lookup.

### 3.6 Your profile (only if you opt in)
My Profile (Coordination, Library and Wayfinder) holds your full name, preferred name, e-mail, company or studio, role, Revit experience and how you found us. It is stored encrypted on your computer and is shared by the B45 Labs products on that computer. It is sent to B45 Labs **only if you turn on "Also sync my profile"** (off by default; it also needs the usage switch to be on), and again each time you save it. Connect has no profile.

### 3.7 Feedback you send
**Send Feedback** (Coordination and Library, in the Help panel and in About Me) sends the message you write, the product, plug-in and Revit versions, your language and the installation identifier, plus the name, company and e-mail if you fill them in. It works even when the usage switch is off, because sending it is your own action. The optional "Include diagnostics" box is off by default; when ticked it adds your operating system, culture and the last error the plug-in logged (file paths, Revit file names and e-mail addresses removed). In Wayfinder, Send Feedback opens your e-mail app instead.

### 3.8 What the usage switch does
- **Coordination and Library:** when it is off, nothing is uploaded and no location lookup is made. Records already kept on your computer stay there and are sent if you turn the switch on again. **Erase my data** removes them.
- **Connect and Wayfinder:** when it is off, they stop recording and empty their waiting queues, and any report older than 3 days is dropped.

## 4. Updates, notices and the remote lock

At start-up each product asks our server whether a newer version exists. Coordination, Library and Connect also ask whether there is an announcement, and Coordination checks for notices about once a minute while Revit is open. Wayfinder asks once, at start-up, and has no announcement check. These requests carry no identifier, but our server and GitHub see your IP address as any website does, and **they are not stopped by the usage switch**.

If you click **Update now** in Coordination, Library or Connect, the installer is downloaded from github.com, checked (SHA-256 and signature) and started; if anything is unexpected, the download page opens instead. Updating needs no administrator rights. In Wayfinder, **Update now** opens the download page in your browser, and you download and run the installer yourself.

B45 Labs can mark a version as no longer allowed. Such a version shows a notice and, for a version withdrawn for safety, **locks its commands until you update**.

## 5. Connect and third-party AI providers

Connect lets you use an in-Revit Assistant and an MCP server with **AI providers and AI clients that you choose**. These are independent controllers under their own terms and privacy policies.

- **The Assistant** uses **Anthropic** or **OpenAI** with **your own API key**. When you send a message, your prompt, the conversation so far and the results of the tools it runs (element counts, ids, findings, and the names and parameter values you ask about) go to that provider directly from your computer. They do not pass through B45 Labs.
- **Voice dictation** uploads the recorded audio to OpenAI with your key, only while you dictate. Without an OpenAI key, Windows speech recognition is used and no audio leaves your computer.
- **External MCP clients** (Claude Desktop, Claude Code, Codex, Cursor, VS Code, Windsurf, Gemini CLI and others) receive tool results on your computer over a local named pipe and pass them to their own provider under your account. These clients receive reading, checking, audit and view-only tools. None creates, edits or deletes model elements by default; changes stay inside Revit behind a confirmation card.
- **Your keys** are stored encrypted on your computer with Windows DPAPI for your Windows user. We never receive them.
- **Your chats** are kept as files on your computer in `%LocalAppData%\B45Labs\Connect\history`, not password protected, and never sent to B45 Labs. Delete the folder at any time.

If you do not set a key, do not use the Assistant or dictation and do not connect an external client, no prompt, model data or audio leaves your computer through Connect.

## 6. What we do not collect

- Your project contents, drawings, geometry or BIM data.
- Model or family file names, file paths or folder locations. The only exception is the content of an error message, which can name an element, view or family (section 3.2).
- Payment information.
- Precise location, a city, passwords or credentials.
- Your Revit, Navisworks or Windows user name, or your computer name.
- Hardware details or operating-system details, except the optional diagnostics in 3.7.

If such information appears in a screenshot or log you send us for support, please remove it first.

## 7. The Website (b45labs.com)

- **Forms** (newsletter, demo, services, live invitation, roadmap request, testimonial): we store what you type (name, e-mail, company, message, location) with the language of the page and your country. Your country is looked up from your IP address by **get.geojs.io** when you send a form. If the form cannot be sent, a message may open in your e-mail app with what you typed.
- **Visits** are counted with Plausible Analytics, without cookies.
- **Fonts and videos** load from Google Fonts and YouTube, which see your IP address. Some pages load a library from jsDelivr.
- **Your browser** stores your theme, the notices you closed and a random identifier used to count roadmap votes.
- Forms are stored in our Bubble backend. To see or delete what you sent, write to support@b45labs.com.

## 8. How we use information

- Measuring feature adoption to prioritize development, and planning the roadmap.
- Improving stability, performance and reliability across Revit and Navisworks versions.
- Finding and fixing errors, and supporting you.
- Checking that installers and updates reach people safely.
- Answering the messages and requests you send.
- Producing **aggregated, de-identified statistics**, including for the publication and research uses in section 8.1.

### 8.1 Aggregated statistics, publication and research
B45 Labs may combine data from many installations into aggregated, de-identified statistics, such as the number of installations and sessions, the continents, countries and states or provinces where the Software is used, the most-used commands, version adoption and usage trends over time ("Aggregated Statistics").

B45 Labs may publish and disclose Aggregated Statistics, including on its website, in product, business and professional materials, and in academic and scientific research such as articles, theses and conference presentations, and the datasets that support them.

Aggregated Statistics:
- never include your profile data, even if you synced it;
- never include the text of error messages or stack traces, only counts and rates of errors;
- never identify you, your employer, your clients or your projects;
- are published only in a form in which no individual or organization can reasonably be identified.

We do not try to re-identify anyone from Aggregated Statistics. Turning off "Share usage data" keeps your installation out of the statistics produced after that point. Statistics already published cannot be withdrawn, because they contain nothing that can be traced back to you.


## 9. Sharing and service providers

We do not sell your data and we do not share it with third parties for advertising or marketing. We use these providers to run the Software and the Website:

| Provider | What it does | What it sees |
|---|---|---|
| Bubble (United States) | Our backend: usage and error records, installation records, optional profiles, feedback, forms, newsletter | The data described in this policy, and your IP address with each request |
| ipwhois.app | Region lookup from the Software | Your IP address |
| get.geojs.io | Country lookup for Website forms | Your IP address |
| GitHub | Hosts installers and updates | Your IP address when you download |
| Plausible Analytics | Website visit counts | Page visits, without cookies |
| Google Fonts, YouTube, jsDelivr | Fonts, videos and a map library on the Website | Your IP address |
| Anthropic, OpenAI | Only if you use Connect's Assistant, dictation or tunnel, with your own account | What you send them (section 5) |

ipwhois.app and get.geojs.io are public services that we call without an account or key; they see your IP address as any website you visit does. We may disclose information if required by law or to protect our rights and the security of the Software.

## 10. How long we keep data

We keep usage, error, installation, profile, feedback and form data for **up to 36 months** and then delete it. We delete it earlier when you ask (section 12). Aggregated Statistics contain no personal data and may be kept indefinitely.

On your computer, files stay until you remove them: Erase my data removes the B45 Labs data; the Connect files (keys, chats, logs) can be deleted by hand; uninstalling the Software leaves your settings and profile so a reinstall finds them.

## 11. Security

Data is sent over encrypted (HTTPS/TLS) connections, your profile and API keys are encrypted at rest on your computer, and error data is sanitized as described in 3.2. Collected data is stored on access-controlled infrastructure available only to authorized people. No method of transmission or storage is completely secure.

## 12. Your choices and requests

From **My Profile**:
- **Share usage data**: master switch for usage reporting (section 3.8).
- **Also sync my profile**: off by default.
- **Export my data**: a JSON file with what is stored locally about you.
- **Erase my data**: permanently deletes all B45 Labs data stored on your computer (profile, usage history and machine identity) and asks our server to delete the records linked to your installation identifier. This cannot be undone. Because the profile, identifier and privacy choice are shared, this covers the other B45 Labs products on the same computer.

Newsletter sign-ups, forms you sent from the website and feedback you sent are deleted on request: write to **support@b45labs.com**. You may also ask what we hold about you, or ask us to correct it. We may ask for information to verify your request.

## 13. International transfers

The Software and the Website are used in many countries. Our backend is in the United States, and the other providers in section 9 operate where they are.

## 14. Changes to this policy

We may update this policy. The "Last updated" date shows the latest revision. Material changes, including any new kind of data collection, will be announced in release notes or in the Software before the collection starts.

## 15. Contact

B45 Labs Support, **support@b45labs.com**.

## Annex: Files that Connect stores on your computer

The usage queue and the failure queue are sent as described in sections 3.1 and 3.2. Everything else below is never transmitted to B45 Labs:

- **Your AI provider API keys**, one encrypted file per provider under `%LocalAppData%\B45Labs\Connect\`, protected with Windows DPAPI for your Windows user account (section 5).
- **Your microphone preference** for voice dictation, remembered on this PC.
- **The MCP server log**, `%AppData%\B45Labs\Connect\mcp_server.log` (rotated once to `mcp_server.1.log` at 1 MB). Each line carries a timestamp, the tool name, the outcome and the elapsed time; **never** the arguments sent or the results returned, so no model data lands in it.
- **The add-in error log**, `%AppData%\B45Labs\Connect\connect_errorlog.jsonl`, sanitised (file paths, model names and e-mail addresses are redacted when written).
- **The installation memory**, `%LocalAppData%\B45Labs\Connect\installation_sent.json`: what Connect last sent in its installation record (versions, dates, language, the installation identifier). It holds no content and is never sent as a file.
- **The usage queue**, `%LocalAppData%\B45Labs\Connect\usage_queue.jsonl`: the counts waiting to be sent (one short line per event, no content). It is emptied after each successful send, capped at 256 KB, and nothing is written to it while the usage switch is off.
- **The failure queue**, `%LocalAppData%\B45Labs\Connect\failure_queue.jsonl`: the short failure reports of section 3.2 waiting to be sent (no message text and no content). Reports older than 3 days are dropped, and nothing is written to it while the usage switch is off.
- **Your chat history**, `%LocalAppData%\B45Labs\Connect\history\`: your conversations with the Assistant (what you saw in the chat: your messages, the answers and the tool and error lines), kept on this PC so that "New chat" does not throw the previous one away. A chat can include names and numbers from your models, and the files are not protected with a password. They are never sent to B45 Labs; delete the folder, or the chats you do not want, at any time.
- **An entry in Claude Desktop's configuration file** (`%AppData%\Claude\claude_desktop_config.json`) only when you click “Enable in Claude Desktop”; “Disable” removes it. The Software edits no other third-party configuration file.
- **The embedded documentation index**: an offline copy of the B45 Labs command documentation shipped inside the add-in, which the Assistant reads locally to explain a command. It makes no network request.

You can delete the log files at any time; they are recreated on the next run. Uninstalling removes the add-in and the MCP server; the key files and logs listed above may remain under your user folders and can be deleted by hand.

## Annex: What Wayfinder stores on your computer

| Data | Where | Why | Protected | How to remove |
|---|---|---|---|---|
| Your settings (FlyNav speeds, clash box distances, hidden prompts) | `%LOCALAPPDATA%\B45Labs\B45Wayfinder\settings.ini` | Remember your preferences | Plain text, no personal data | Delete the file, or uninstall and delete the folder |
| Rows waiting to be sent, and the installation facts above | `%LOCALAPPDATA%\B45Labs\B45Wayfinder\telemetry\` | Send them when you are online (rows older than 3 days are dropped) | Plain text, tied to a random install ID, no name or e-mail | My Profile > Erase my data |
| The installation ID | Shared with the other B45 Labs products (`%APPDATA%\B45Labs\installation_state.json`); if Wayfinder is the first one installed, `HKCU\Software\B45Labs` | One ID for the whole suite | A random number | My Profile > Erase my data |
| Log files | `%LOCALAPPDATA%\B45Labs\B45Wayfinder\logs\` | Help you and B45 Labs support find a problem. You decide whether to send a log. | Plain text; may contain model/item names that appear in an error. **Logs are never sent.** | Delete the folder |
| My Profile (name, role, preferences you type) and your logo | `%APPDATA%\B45Labs\user-profile.enc` and `%APPDATA%\B45Labs\branding\` | Greeting and branding inside the tools. **Shared with the other B45 Labs products on this computer**: what you fill in in one shows in all | Profile encrypted with Windows DPAPI (current user only) | My Profile > Erase my data |
| Your privacy choice | `%APPDATA%\B45Labs\telemetry_consent.json` | Remember whether you turned data sharing off. **Shared with the other B45 Labs products**: one choice for all | Local file | My Profile > Privacy |

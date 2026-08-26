# Clone customization

Each cloned bot gets its own settings document, keyed by the cloned bot's Telegram ID.

Open `/clonesettings` in the clone as its owner/admin.

Supported:
- `/set_start <text>`
- `/set_help <text>`
- `/set_about <text>`
- `/set_file_message <text>`
- `/set_verify_message <text>`
- `/set_autodelete 600` or `/set_autodelete off`
- `/set_verify on` or `/set_verify off`
- `/set_startbutton Button text | https://example.com`
- `/clear_startbuttons`

Placeholders:
- `{mention}`
- `{first_name}`
- `{username}`

The existing auto-filter, indexing, force-subscription and clone features are retained.
The new settings are persisted in MongoDB under `cloned_bots.clone_settings`.

Important: configure your normal `API_ID`, `API_HASH`, `BOT_TOKEN`, `DATABASE_URI` and other
environment variables exactly as required by the original project. Never commit bot tokens.

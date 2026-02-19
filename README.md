# Documenso (YunoHost custom app)

This app runs Documenso in Docker with a path-based reverse proxy.

- Install path e.g. `/sign`
- Optional SMTP (config panel). Hinweis: Bei YunoHost-Postfix meist **127.0.0.1:25** (nicht localhost)
- SQLite storage under app data dir
- SSO disabled on the app's domain (required for public access on some setups)


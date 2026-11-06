# Vekrun releases

Signed Vekrun desktop builds and the update feeds the installed app reads.
This repository holds **binaries and feeds only** — no source code.

- **Releases** (`v<version>`) carry the installers (`.dmg`) and the signed
  update archives (`.app.tar.gz` + `.sig`) per platform. A release is never
  replaced; a fix ships as a new version.
- **`feeds/<channel>.json`** (`alpha`, `stable`) tells the app which version
  is current on its channel. A feed changes in one commit, only after every
  file it points to has been uploaded and verified.

Every update is checked by the app against the signing key built into it
before it is installed; a file that does not verify is refused.

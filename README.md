# theodia.playlists

Public playlist repository for [Theodia](https://theodia.app). This repo distributes `.playlist.zip` packages that users can install directly inside the app through **Settings → Resources → Install from GitHub → Playlists**.

## What is a playlist?

A playlist is a named, ordered list of spoken tracks. Each track can be plain text or a Bible passage. Playlists are played back by the built-in Playlist feature using text-to-speech. For the full feature design, see [`notes/playlist-design.md`](https://github.com/ecodiallc/TheodiaApp/blob/main/notes/playlist-design.md) in the main app repository.

## Install a playlist

1. Open Theodia.
2. Go to **Settings → Resources → Install from GitHub**.
3. Select the **Playlists** tab.
4. Tap the playlist you want, then tap **Install**.

You can also add a custom playlist repo under **Settings → GitHub → Add Repository**.

## Playlists available here

This repository is currently a placeholder. Packaged playlists are being maintained in [`otseng/theodia.playlists`](https://github.com/otseng/theodia.playlists).

See the full list and metadata in [`index.json`](index.json).

## Want to contribute?

Playlist ideas, design principles, and packaging instructions are documented in the main app repo:

- [`notes/playlist-ideas.md`](https://github.com/ecodiallc/TheodiaApp/blob/main/notes/playlist-ideas.md) — backlog of high-value playlist concepts
- [`notes/playlist-development.md`](https://github.com/ecodiallc/TheodiaApp/blob/main/notes/playlist-development.md) — internal contributor workflow
- [`notes/migrate-playlists-to-github.md`](https://github.com/ecodiallc/TheodiaApp/blob/main/notes/migrate-playlists-to-github.md) — distribution design
- [`notes/github-repo-naming-standards.md`](https://github.com/ecodiallc/TheodiaApp/blob/main/notes/github-repo-naming-standards.md) — file naming rules

## Package format

Each `.playlist.zip` contains:

- One `.playlist.json` file in the `PlaylistBackupSnapshot` shape (`{ playlists: Playlist[] }`).
- Optional `.mp3` audio files referenced by tracks using bare filenames.

The app imports the snapshot into its local `playlist.sqlite` database and copies MP3 files to the imported audio directory.

## License

Playlists distributed from this repository are © Theodia unless otherwise noted in the individual package metadata. Scripture quotations remain in the public domain or under the terms of the Bible module used.

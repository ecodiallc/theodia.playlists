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

| Playlist | Category | Description |
| -------- | -------- | ----------- |
| [10 Core Memory Verses](10-Core-Memory-Verses.playlist.zip) | Memory | Ten of the most frequently memorized verses, each spoken twice with a brief pause. |
| [23rd Psalm Variations](23rd-Psalm-Variations.playlist.zip) | Memory | Psalm 23 read once, then a plain-text meditation on its key images. |
| [Armor of God](Armor-Of-God.playlist.zip) | Foundations | Ephesians 6:10-18 read and then each piece of armor unpacked. |
| [Bedtime Psalms](Bedtime-Psalms.playlist.zip) | Daily | Gentle Psalms and short restful passages, with a slow, quiet framing. |
| [Benedictions and Blessings](Benedictions-And-Blessings.playlist.zip) | Worship | Scripture blessings to send someone off, end a meeting, or close a day. |
| [Comfort in Sorrow](Comfort-In-Sorrow.playlist.zip) | Comfort | Verses about God's nearness in grief, anxiety, and loss. |
| [Genesis: Beginnings](Genesis-Beginnings.playlist.zip) | Overview | A curated playlist of Genesis 1-11 highlights: creation, fall, flood, Babel, and the call of Abraham. |
| [Morning Commute Devotional](Morning-Commute-Devotional.playlist.zip) | Daily | A five-minute starter for the day: greeting, a Psalm, a short Gospel reflection, and a sending blessing. |
| [Prodigal Son](Prodigal-Son.playlist.zip) | Gospel | A curated playlist about the parable of the Prodigal Son. |
| [The Beatitudes](The-Beatitudes.playlist.zip) | Virtue | Matthew 5:3-12 read as a single unit, then each beatitude repeated with a one-line reflection. |
| [The Fruit of the Spirit](The-Fruit-Of-The-Spirit.playlist.zip) | Virtue | Galatians 5:22-23 unpacked with one short passage or reflection per fruit. |
| [The Good News in Ten Verses](The-Good-News-In-Ten-Verses.playlist.zip) | Gospel | A concise redemption narrative from creation to restoration. |
| [The Lord's Prayer](The-Lords-Prayer.playlist.zip) | Memory | The Lord's Prayer from Matthew 6, spoken slowly, then phrase by phrase. |
| [The Parables of Jesus](The-Parables-Of-Jesus.playlist.zip) | Gospel | A sampler of Jesus' parables with brief context tracks. |
| [The Psalms of Praise](The-Psalms-Of-Praise.playlist.zip) | Worship | A short collection of Psalms focused on praise and thanksgiving. |
| [Words for a Good Life](Words-For-A-Good-Life.playlist.zip) | Wisdom | Proverbs selections on speech, work, friendship, money, and humility. |

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

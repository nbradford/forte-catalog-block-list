# forte-catalog-block-list

The shared block list [Forte](https://github.com/nbradford/Forte) uses to keep spam and AI-generated "artists" out of its New Releases feed.

## How Forte uses it

- Forte downloads [`blocklist.json`](blocklist.json) when it launches, and whenever you pull to refresh in **Settings › Blocked Artists**. Syncing is on by default and can be switched off there.
- A blocked artist's releases are hidden everywhere they're credited — as the main artist, a collaborator, or a featured guest.
- Your own choices always win. Allow any artist from this list in **Settings › Blocked Artists** and their releases stay visible on your device, no matter what the list says.
- The request carries nothing about you, your library, or your listening history.

## Format

```json
{
  "artists" : ["Artist Name", "Another Artist"],
  "version" : 1
}
```

Names are matched case-insensitively against Apple Music's artist credits. Blank entries and duplicates are ignored.

## Updating the list

In Forte, open **Settings › Blocked Artists**, tap the share button to export your blocks as `blocklist.json`, and commit that file here.

## Suggesting an artist

Open an issue with the artist's name as it appears in Apple Music and a link to one of their releases.

# MALToAnything
Search by MyAnimeList ID in Anilibria, SovetRomantica and possibly other providers

Shikimori ID is the same as MAL ID.

## Anilibria

Covers all releases from 2001 to 2025

Currently has **1671 entries**.

First 246 of entries were mapped manually, and then i got tired of it and made automatic mapping

The results of automatic mappings were insane: when searching only manually mapped IDs, they precisely matched with ~220 manually mapped entries, with 1 being different (and it was actually my mistake - i confused that anime with another season) and others being not found. When searching all 2001-2025 releases, they found ~1540 animes and did not find ~180 (i manually mapped them)

68 entries don't exist on MAL (such as Sanyok & Boryan, korean/chinese dramas, american animes, non-animated shows/movies and other things)

Schema:

```ts
{
  idMal:       integer().notNull().unique(),
  idAnilibria: integer().notNull(),
}
```

## SovetRomantica

Covers all releases that had an `anime_shikimori` property in the SovetRomantica API response

Currently has **1329 entries**.

Shikimori ID is the same as MyAnimeList ID

Schema:

```ts
{
  idShikimori: integer().notNull().unique(),
  idSR:        integer().notNull().unique(),
}
```

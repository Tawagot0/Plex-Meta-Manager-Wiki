You can build different collections using the features of [AniDB.net](https://anidb.net/) (AniDB).

No configuration is required for these builders.

| Name | Attribute | Description | Works with Movies | Works with Shows |
| :--- | :--- | :--- | :---: | :---: |
| [AniDB ID](#anidb-id) | `anidb_id` | Gets the anime specified by the AniDB ID | :heavy_check_mark: | :heavy_check_mark: |
| [AniDB Relation](#anidb-relation) | `anidb_relation` | Gets all anime in the relation graph of the specified AniDB ID | :heavy_check_mark: | :heavy_check_mark: |
| [AniDB Popular](#anidb-popular) | `anidb_popular` | Gets every anime in AniDB's [Popular Anime](https://anidb.net/latest/anime/popular/?h=1) list | :heavy_check_mark: | :heavy_check_mark: |
| [AniDB Tags](#anidb-tags) | `anidb_tags` | Gets every anime in a AniDB Tag | :heavy_check_mark: | :heavy_check_mark: |

## AniDB ID
Gets the anime specified by the AniDB ID.

The expected input is an AniDB ID or AniDB Anime URL. Multiple values are supported as either a list or a comma-separated string.

```yaml
collections:
  Sword Art Online Shows:
    anidb_id: 8692, 8691, 13494
```
```yaml
collections:
  Sword Art Online Shows:
    anidb_id: https://anidb.net/anime/8692, https://anidb.net/anime/8691, https://anidb.net/anime/13494
```

## AniDB Relation
Gets all anime in the relation graph of the specified AniDB ID.

To see the relation graph of an anime use: `https://anidb.net/anime/<ANIDB_ID>/relation/graph` but replace `<ANIDB_ID>` with the AniDB ID you want to see the relations for.

The expected input is an AniDB ID, AniDB Anime URL, or AniDB Anime Relation URL. Multiple values are supported as either a list or a comma-separated string.

```yaml
collections:
  All Sword Art Online:
    anidb_relation: 8692
```
```yaml
collections:
  All Sword Art Online:
    anidb_relation: https://anidb.net/anime/8692
```
```yaml
collections:
  All Sword Art Online:
    anidb_relation: https://anidb.net/anime/8692/relation/graph
```

## AniDB Popular
Gets every anime in AniDB's [Popular Anime](https://anidb.net/latest/anime/popular/?h=1) list.

The expected input is a single integer value of how much anime to query with a max of 30.

The `sync_mode: sync` option is also recommended since the Trakt Trending lists are continuously updated.

```yaml
collections:
  AniDB Popular:
    anidb_popular: 30
    sync_mode: sync
```


## AniDB Tag
Gets anime with the specified AniDB Tag the options are detailed below. 

| Attribute | Description | Required | Default |
| :--- | :--- | :---: | :---: |
| `tag` | AniDB Tag ID to search by | :heavy_check_mark: | N/A |
| `limit` | Number of Anime to query from AniDB (use 0 for all; max: 500) | :x: | 0 |

```yaml
collections:
  Pirates Anime:
    anidb_tag:
      tag: 1700
      limit: 500
    sync_mode: sync
```

* To find possible tags go to the [AniDB Anime](https://anidb.net/tag) page to find the tags available. Copy the link and find the tag ID at the end of the url.

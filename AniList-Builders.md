You can build different collections using the features of [AniList.co](https://anilist.co/) (AniList).

No configuration is required for these builders.

| Name | Attribute | Description | Works with Movies | Works with Shows |
| :--- | :--- | :--- | :---: | :---: |
| [AniList Top Rated Anime](#anilist-top-rated-anime) | `anilist_top_rated` | Gets every anime in AniList's [Top Rated Anime](https://anilist.co/search/anime?sort=SCORE_DESC) list | :heavy_check_mark: | :heavy_check_mark: |
| [AniList Popular Anime](#anilist-popular-anime) | `anilist_popular` | Gets every anime in AniList's [Popular Anime](https://anilist.co/search/anime?sort=POPULARITY_DESC) list | :heavy_check_mark: | :heavy_check_mark: |
| [AniList Relations](#anilist-relations) | `anilist_relations` | Gets the anime specified by the AniList ID and every relation in its relation tree except Character and Other relations | :heavy_check_mark: | :heavy_check_mark: |
| [AniList Studio](#anilist-studio) | `anilist_studio` | Gets all anime specified by the AniList Studio ID | :heavy_check_mark: | :heavy_check_mark: |
| [AniList ID](#anilist-id) | `anilist_id` | Gets the anime specified by the AniList ID | :heavy_check_mark: | :heavy_check_mark: |
| [AniList Search](#anilist-search) | `anilist_search` | Gets the anime specified by the AniList search parameters provided | :heavy_check_mark: | :heavy_check_mark: |

## AniList Top Rated Anime
Gets every anime in AniList's [Top Rated Anime](https://anilist.co/search/anime?sort=SCORE_DESC) list.

The expected input is a single integer value of how many movies/shows to query. 

The `sync_mode: sync` option is also recommended since the Trakt Watched lists are continuously updated.

```yaml
collections:
  Top Rated Anime:
    anilist_top_rated: 30
    sync_mode: sync
```

## AniList Popular Anime
Gets every anime in AniList's [Popular Anime](https://anilist.co/search/anime?sort=POPULARITY_DESC) list.

The expected input is a single integer value of how many movies/shows to query. 

The `sync_mode: sync` option is also recommended since the Trakt Watched lists are continuously updated.

```yaml
collections:
  Popular Anime:
    anilist_popular: 10
    sync_mode: sync
```

## AniList Relations
Gets the anime specified by the AniList ID and every relation in its relation tree except Character and Other relations.

The expected input is an AniList ID. Multiple values are supported as either a list or a comma-separated string.

```yaml
collections:
  One Piece:
    anilist_relations: 21
```

## AniList Studio
Gets all anime specified by the AniList Studio ID.

The expected input is an AniList ID. Multiple values are supported as either a list or a comma-separated string.

```yaml
collections:
  Studio Ghibli:
    anilist_studio: 21
```

## AniList ID
Gets the anime specified by the AniList ID.

The expected input is an AniList ID. Multiple values are supported as either a list or a comma-separated string.

```yaml
collections:
  Cowboy Bebop:
    anilist_id: 23, 219
```

## AniList Search
Gets the anime specified by the AniList Search the options are detailed below. 

There are three fields per search option when using AniList's Search just like Plex's Advance Filters in the Web UI. The first is the **Attribute** (what attribute you wish to search), the second is the **Modifier** (which modifier to use), and the third is the **Term** (actual term to search).

| Attribute | Description | Options | Default |
| :--- | :--- | :---: | :---: |
| `sort_by` | How to sort the Anime | `score` (Sort by Average Score)<br>`popular` (Sort by Popularity) | `score` |
| `limit` | Number of Anime to query | `int` (use 0 or don't use it at all for all anime) | `0` |
| `search` | Text to search | Any Text | `N/A` | 
| `season` | Season to search for | `winter` (For winter season December, January, February)<br>`spring` (For spring season March, April, May)<br>`summer` (For summer season June, July, August)<br>`fall` (For fall season September, October, November)<br>Leave blank for the Current Season |
| `year` | Season year to search for | `int` `1917` - next year or leave blank for the current year | 
| `min_tag_percent` | Minimum tag percentage for the Anime | `int` `0`-`100` | `N/A` |
| `adult` | Search for or not for Adult Anime | `true` or `false` | `N/A` |

## Tag Searches
Tag searches can be used with either no modifier or with `.not`.

String search can take multiple values as a **list or a comma-separated string**.

### Tag Modifiers

| Tag Modifier | Description |
| :--- | :--- |
| No Modifier | Matches every item where the attribute matches the given string |
| `.not` | Matches every item where the attribute does not match the given string |

### Tag Attributes

| Tag Search | Description | Options | 
| :--- | :--- | :---: |
| `format` | Uses the anime's format to match | `tv`, `short`, `movie`, `special`, `ova`, `ona`, `music` |
| `status` | Uses the anime's status to match | `finished`, `airing`, `not_yet_aired`, `cancelled`, `hiatus` |
| `genre` | Uses the anime's genre to match | Any Genre in the Genre Dropdown box on the [AniList Search Page](https://anilist.co/search/anime) |
| `tag` | Uses the anime's tag to match | Any Tag in the Genre Dropdown box on the [AniList Search Page](https://anilist.co/search/anime) |
| `tag_category` | Uses the anime's tag category to match | Any Tag Category in the Advance Genres & Tag Filters Menu on the [AniList Search Page](https://anilist.co/search/anime) |

## Date Searches
Date searches can be used with either `.before`, or `.after`.

No date search can take multiple values.

### Date Modifiers

| Date Modifier | Description | Format |
| :--- | :--- | :---: |
| `.before` | Matches every item where the date attribute<br>is before the given date | **Format:** MM/DD/YYYY<br>e.g. `01/01/2000` |
| `.after` | Matches every item where the date attribute<br>is after the given date | **Format:** MM/DD/YYYY<br>e.g. `01/01/2000` |

### Date Attributes

| Date Search | Description |
| :--- | :--- |
| `start` | Uses the anime start date attribute to match |
| `end` | Uses the anime end date attribute to match |

## Number Searches
Number searches must use `.gt`, `.gte`, `.lt`, or `.lte` as a modifier.

No number search can take multiple values.

### Number Modifiers

| Number Modifier | Description | Format |
| :--- | :--- | :---: |
| `.gt` | Matches every item where the number attribute<br>is greater then the given number | **Format:** number<br>e.g. `30`, `1995`, or `7.5` |
| `.gte` | Matches every item where the number attribute<br>is greater then or equal to the given number | **Format:** number<br>e.g. `30`, `1995`, or `7.5` |
| `.lt` | Matches every item where the number attribute<br>is less then the given number | **Format:** number<br>e.g. `30`, `1995`, or `7.5` |
| `.lte` | Matches every item where the number attribute<br>is less then or equal to the given number | **Format:** number<br>e.g. `30`, `1995`, or `7.5` |

### Number Attributes

| Number Search | Description | Restrictions |
| :--- | :--- | :---: |
| `duration` | Uses the duration attribute to match using minutes | minimum: `1` |
| `episodes` | Uses the number of episodes attribute to match | minimum: `1` |
| `score` | Uses the score attribute to match | minimum: `1` |
| `popularity` | Uses the popularity attribute to match | minimum: `1` |

## AniList Search Examples

```yaml
collections:
  Current Anime Season:
    anilist_search:
      season:
      year:
      sort_by: popular
    sync_mode: sync
```
```yaml
collections:
  Fall 2020 Anime:
    anilist_search:
      season: fall
      year: 2020
    sync_mode: sync
```
```yaml
collections:
  Pirates Anime:
    anilist_search:
      tag: Pirates
      sort_by: popular
    sync_mode: sync
```
```yaml
collections:
  Top Sports Anime:
    anilist_genre:
      genre: Sports
      limit: 20
      sort_by: popular
    sync_mode: sync
```

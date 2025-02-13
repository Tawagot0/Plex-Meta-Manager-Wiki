# Plex Meta Manager Wiki

This wiki should tell you everything you need to know about the script to get it working.

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/meisnate12/Plex-Meta-Manager?style=plastic)](https://github.com/meisnate12/Plex-Meta-Manager/releases)
[![GitHub commits since latest release (by SemVer)](https://img.shields.io/github/commits-since/meisnate12/plex-meta-manager/latest/develop?label=Number%20of%20Commits%20in%20Develop&style=plastic)](https://github.com/meisnate12/Plex-Meta-Manager/tree/develop)
[![Docker Image Version (latest semver)](https://img.shields.io/docker/v/meisnate12/plex-meta-manager?label=docker&sort=semver&style=plastic)](https://hub.docker.com/r/meisnate12/plex-meta-manager)
[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/meisnate12/plex-meta-manager?style=plastic)](https://hub.docker.com/r/meisnate12/plex-meta-manager)
[![Discord](https://img.shields.io/discord/822460010649878528?label=Discord&style=plastic)](https://discord.gg/TsdpsFYqqm)
[![Donate](https://img.shields.io/badge/-Sponsor_or_Donate-blueviolet?style=plastic)](https://github.com/sponsors/meisnate12)

## Getting Started

1. Install Plex Meta Manager either by installing Python3 and following the [Local Installation Guide](https://github.com/meisnate12/Plex-Meta-Manager/wiki/Local-Installation)
   or by installing Docker and following the [Docker Installation Guide](https://github.com/meisnate12/Plex-Meta-Manager/wiki/Docker-Installation) or the [unRAID Installation Guide](https://github.com/meisnate12/Plex-Meta-Manager/wiki/unRAID-Installation).
2. Once installed, you have to create a [Configuration File](https://github.com/meisnate12/Plex-Meta-Manager/wiki/Configuration-File) filled with all your values to connect to the various services. 
3. After that you can start updating Metadata and building automatic Collections by creating a [Metadata File](https://github.com/meisnate12/Plex-Meta-Manager/wiki/Metadata-File) for each Library you want to interact with.
4. Explore the [Wiki](https://github.com/meisnate12/Plex-Meta-Manager/wiki) to see all the different Collection Builders that can be used to create collections. 

## Support

* Before posting on Github about an enhancement, error, or configuration question please visit the [Plex Meta Manager Discord Server](https://discord.gg/TsdpsFYqqm).
* If you're getting an Error or have an Enhancement post in the [Issues](https://github.com/meisnate12/Plex-Meta-Manager/issues).
* If you have a configuration question post in the [Discussions](https://github.com/meisnate12/Plex-Meta-Manager/discussions).
* To see user submitted Metadata configuration files, and you to even add your own, go to the [Plex Meta Manager Configs](https://github.com/meisnate12/Plex-Meta-Manager-Configs).
* Pull Request are welcome but please submit them to the develop branch.
* If you wish to contribute to the Wiki please fork and send a pull request on the [Plex Meta Manager Wiki Repository](https://github.com/meisnate12/Plex-Meta-Manager-Wiki).

## Table of Contents
- [Home](Home)
- [Local Installation](Local-Installation)
- [Docker Installation](Docker-Installation)
- [unRAID Installation](unRAID-Installation)
- [Configuration File](Configuration-File)
  - [Libraries Attributes](Libraries-Attributes)
  - [Settings Attributes](Settings-Attributes)
  - [Plex Attributes](Plex-Attributes)
  - [TMDb Attributes](TMDb-Attributes)
  - [Radarr Attributes](Radarr-Attributes)
  - [Sonarr Attributes](Sonarr-Attributes)
  - [Tautulli Attributes](Tautulli-Attributes)
  - [OMDb Attributes](OMDb-Attributes) 
  - [Trakt Attributes](Trakt-Attributes)
  - [AniDB Attributes](AniDB-Attributes)
  - [MyAnimeList Attributes](MyAnimeList-Attributes)
- [Metadata File](Metadata-File)
  - [Metadata Attributes](Metadata-Attributes)
    - [Seasons Attributes](Seasons-Attributes)
    - [Episodes Attributes](Episodes-Attributes)
  - [Template Attributes](Template-Attributes)
  - [Collection Attributes](Collection-Attributes)
    - [Collection Builders](Collection-Builders)
      - [Plex Builders](Plex-Builders)
      - [Smart Builders](Smart-Builders)
      - [TMDb Builders](TMDb-Builders)
      - [TVDb Builders](TVDb-Builders)
      - [IMDb Builders](IMDb-Builders)
      - [Trakt Builders](Trakt-Builders)
      - [Tautulli Builders](Tautulli-Builders)
      - [Letterboxd Builders](Letterboxd-Builders)
      - [ICheckMovies Builders](ICheckMovies-Builders)
      - [StevenLu Builders](StevenLu-Builders)
      - [AniDB Builders](AniDB-Builders)
      - [AniList Builders](AniList-Builders)
      - [MyAnimeList Builders](MyAnimeList-Builders)
    - [Collection Details](Collection-Details)
      - [Schedule Detail](Schedule-Detail)
      - [Image Overlay Detail](Image-Overlay-Detail)
    - [Collection Filters](Collection-Filters)
- [Acknowledgements](Acknowledgements)
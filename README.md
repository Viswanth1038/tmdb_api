![Dart pub analyser](https://github.com/Arunnaidu3470/tmdb_api/workflows/Dart%20pub%20analyser/badge.svg?branch=master)
![Run Tests CI](https://github.com/RatakondalaArun/tmdb_api/workflows/Run%20Tests%20CI/badge.svg)
[![pub package](https://img.shields.io/pub/v/tmdb_api?color=dark%20green&include_prereleases&label=pub%20package&logo=dart)](https://pub.dartlang.org/packages/tmdb_api)

# tmdb_api
<img src="https://www.themoviedb.org/assets/2/v4/logos/v2/blue_square_2-d537fb228cf3ded904ef09b136fe3fec72548ebc1fea3fbbd1ad9e36364db38b.svg" height=100px width="50%"><img src="https://dart.dev/assets/shared/dart/logo+text/horizontal/white-e71fb382ad5229792cc704b3ee7a88f8013e986d6e34f0956d89c453b454d0a5.svg" height="100px" width="50%">

A TheMovieDatabase client library for dart.
To know more about TMDB visit [*offical site*](https://www.themoviedb.org/)

## Avaliable Methods 
### v3( 🎊✨ Completed 🎉🎉)
Supports all the functions of version 3 of tmdb API
- [X] Auth
- [X] Account
- [X] Guest Sessions
- [x] Movies
- [x] Tv shows
- [x] Tv Seasons
- [x] Tv Episodes 
- [X] People
- [X] Credits
- [X] Certification
- [X] Changes
- [X] Collections
- [X] Find
- [X] Genres
- [X] Keywords
- [X] Companies
- [X] Trending
- [X] Search
- [X] Discover
- [X] Networks
- [X] Reviews
- [X] Versions
- [X] Lists
    
### v4(🎊✨ Completed 🎉🎉)
- [X] Image URL Constructor
- [X] auth
- [X] account
- [X] lists

---
# Getting started
_(updated on v1.2.4)_

## Step 1: Adding as dependencies
[Pub.dev's installation guide](https://pub.dev/packages/tmdb_api#-installing-tab-)

Add this to your package's pubspec.yaml file:
```
dependencies:
  tmdb_api: ^1.2.4 //visit tmdb for latest version number
```
## Step 2: Import it
Now in your Dart code, you can use:
```
import 'package:tmdb_api/tmdb_api.dart';
```

## Step 3: Create Instance
Now you need to create instance for `TMDB` and `ApiKeys` with your api keys.

```
TMDB tmdbWithCustomLogs = TMDB( //TMDB instance
    ApiKeys('Your API KEY', 'apiReadAccessTokenv4'),//ApiKeys instance with your keys,
  );
```
## Step 4(Optional): Configuring console logs
There are 3 logconfigs presets avaliable.
- `ConfigLogger.showAll()`: development use.
- `ConfigLogger.showRecommended()`: development use.
- `ConfigLogger.showNone()`: production use.
  
You can add any off this presets to `logConfig` named parameter of `TMDB` instance

**Custom Logs**
```
TMDB tmdbWithCustomLogs = TMDB(
    ApiKeys('Your API KEY', 'apiReadAccessTokenv4'),
    logConfig: ConfigLogger(
      showLogs: true,//must be true than only all other logs will be shown
      showErrorLogs: true,
    ),
  );
```
# Example

For getting Trending movies 
```
Map result = await tmdb.v3.trending.getTrending(mediaType = MediaType.all,timeWindow = TimeWindow.day);

```

# For more API documentation
visit [offical API documentation](https://developers.themoviedb.org/3/getting-started/introduction)
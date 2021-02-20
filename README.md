###### ACCOUNTS
- **account list**
  > Prints a list of accounts saved in Gohan
- **account create [name]**
  > Creates an account and saves it as [name]
- **account load [name]**
  > Loads account named as [name]
###### APK
- **apk download**
  > Downloads the latest game APK from QooApp in the following path : /data/[global|japan]/apk/latest.apk
- **apk decompile**
  > Decompiles /data/[global|japan]/apk/latest.apk in /data/[global|japan]/apk/latest-content/
  (if APK doesnt exist, it downloads it by issuing 'apk download')
- **apk info**
  > Grabs a decompiled APK infos using the following path : /data/[global|japan]/apk/latest-content/
  (in decompiled APK doesnt exist, it decompiles it by issuing 'apk decompile')
###### ASSETS
- **assets refresh**
  > Refreshes assets timestamp to match with the server one.
- **assets download [timestamp]**
  > Downloads game assets from a given timestamp. Enter 0 to download all assets.
- **assets get [query]**
  > Searches through game assets to download a specific asset.
  (when the process is finished, enter 'y' to unpack downloaded assets)
- **assets unpack [optional: path]**
  > [GUI] Unpacks given game assets (CPK/USM/AWB). Tip : input 'all' as path to unpack all assets recursively.
  /!\ if a path is given, it must be like : character/card/100000.cpk (/data/[global/japan]/assets/[PATH])
  (if the given asset doesn't exist, it downloads it by issuing 'assets get [path]')
- **assets repack [path]**
  > Repacks given folder into one CPK. Ex. 'assets repack character/card/thumb/' : packs the content of /data/[global/japan]/assets/character/card/thumb/ into /data/[global/japan]/assets/character/card/thumb.cpk
###### DATABASE
- **database download**
  > Downloads game database in the following path : /data/[global/japan]/database/database.db
- **database decrypt**
  > Decrypts game database. The database must be previously downloaded.
  (if the database is not previously downloaded, it downloads it by issuing 'database download')
###### API
- **login**
  > Logs into the game, and prints current tokens.
- **retrieve [events/news/gashas]**
  > Fetches data of current game events/news/gashas using loaded token.
###### CARDS
- **card info [id]**
  > Prints following infos on a card :
  - Leader skill name
  - Leader skill description
  - Passive skill name
  - Passive skill description
  - Transformation infos
  - Active Skill infos
  - Special Attacks infos
  - EZA infos
  - Links infos
  - Animation files (.lwf,...)
  [TO DO]
- **card art [card id]**
  > Merges parts of a cards by using character,effect,bg.
  (if they don't exist, it unpacks them by issuing 'assets unpack character/card/[card id].cpk')
- **card thumb [card id]**
  > Merges both thumb of the given card & the thumb template.
  (needs thumb of the card, thumb template and game database to fetch card element and rarity.
  if they aren't already downloaded, it downloads them automatically.)
###### MISC
- **config**
  > Prints Gohan's config

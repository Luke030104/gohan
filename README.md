###### ACCOUNTS
- **account list**
  > Prints a list of accounts saved in database
- **account create [name]**
  > Creates an account and saves it as [name] in database
- **account load [name]**
  > Loads account named as [name] in database
###### APK
- **apk download**
  > Downloads the latest game APK from QooApp in the following path : /data/[global|japan]/apk/latest.apk
- **apk decompile**
  > Decompiles /data/[global|japan]/apk/latest.apk in /data/[global|japan]/apk/latest-content/
  (if APK doesnt exist, it downloads it by issuing 'apk download')
- **apk info**
  > Grabs a decompiled APK infos using the following path : /data/[global|japan]/apk/latest-content/
  (if decompiled APK doesnt exist, it decompiles it by issuing 'apk decompile')
- **apk refresh**
  > Downloads, decompiles and grab infos using APK. Refreshes APK hash in case new APK is available.
###### ASSETS
- **assets refresh**
  > Refreshes assets timestamp to match with the server one. If your actual timestamp is not 0 (you already have assets loaded), and new assets are detected, it downloads them.
- **assets download [timestamp]**
  > Downloads game assets from a given timestamp. Enter 0 to download all assets.
- **assets get [query]**
  > Searches through game assets to download specific assets.
- **assets unpack [optional: path]**
  > [GUI] Unpacks given game assets ([!] CPK ONLY). If no path is given, unpacks all assets recursively.
  /!\ if a path is given, it must be like : character/card/100000.cpk (/data/[global/japan]/assets/[PATH])
  (if the given asset doesn't exist, it downloads it by issuing 'assets get [path]')
- **assets repack [path]**
  > Repacks given folder into one CPK. Ex. 'assets repack character/card/thumb/' : packs the content of /data/[global/japan]/assets/character/card/thumb/ into /data/[global/japan]/assets/character/card/thumb.cpk
###### BINARIES
- **binaries [apktool/cpk]**
  > Downloads given binaries.
###### DATABASE
- **database download**
  > Downloads game database in the following path : /data/[global/japan]/database/database.db
- **database decrypt**
  > Decrypts game database in the following path : /data/[global/japan]/database/database.db. The database must be previously downloaded.
  (if the database is not previously downloaded, it downloads it by issuing 'database download')
- **database refresh**
  > Refreshes database timestamp to match with the server one. If your actual timestamp is not 0 (you already have database loaded), and new database is detected, it downloads it.
###### API
- **login**
  > Logs into the game, and prints current tokens.
- **retrieve news [optional: news_id]**
  > Fetches data of given news ID using loaded account in : /data/[global/japan]/news/{news_id}/. If no news ID is given, retrieves every news.
###### CARDS
- **card art [card id]**
  > Merges parts of a cards by using character,effect,bg.
  (if they don't exist, it unpacks them by issuing 'assets unpack character/card/[card id].cpk')
###### MISC
- **config**
  > Prints Gohan's config
- **clear**
  > Clears the CMD.
 - **exit**
  > Restart the program.

![Download icon](/static/img/containers.png)
# News
## LXD 0.5 リリースのお知らせ <!-- LXD 0.5 release announcement --><span class="text-muted">2015 年 3 月 24 日<!-- 24th of March 2015 --></span>

<!--
The major changes for this release are:
-->
このリリースの主な変更点は以下の通りです。

 * IPv6 でリモートサーバを扱えるようになりました <!--  IPv6 support for remote servers -->
 * リモートサーバがシステムが信頼する証明書を持つようになった場合のチェックを行うようにしました <!-- Check if the remote server happens to have a certificate which is trusted by the system -->
 * "lxc image copy" コマンドを実装しました <!-- Implemented "lxc image copy" -->
 * リモートの扱いを改良しました (デフォルトの設定、https:// と unix:// のサポート、多数の使いやすいエイリアス) <!-- Improved remote handling (default configuration, support for https:// and unix:// and a bunch of convenient aliases) -->
 * key/value の保存に対する API の一貫性を確保しました (常にディレクトリとしてエクスポートするようになりました) <!-- API consistency for key/value storage (always exported as dictionaries) -->
 * リモートのイメージが長いハッシュでも短いハッシュでも起動できるようになりました <!-- Remote images can now be started by their long or short hash -->
 * リモートのイメージのプロパティがローカルのキャッシュにきちんとミラーされるようになりました <!-- Remote image properties are now properly mirrored in the local cache -->
 * 多数のデータベースのロック問題が解決されました <!-- A lot of database locking issues have been resolved -->

<!--
Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)
-->
このリリースはまだ LXD 開発の初期であり、現時点の LXD はまだプロダクション用途向きではないことに注意してください。そしてサポートはありません。(報告されたバグ修正やパッチは次のリリースに含まれる予定です)

<!--
At this point, most core LXD features are present but many of the  
particular options aren't implemented yet (don't match our  
specifications), we expect to make great progress in supporting all of  
the expected options over the next couple of releases.
-->
現時点で、ほとんどの LXD の機能の主要なものが提供されるようになりました。しかし、まだ多数の特定のオプションが実装されていません (仕様と一致していません)。今後の数リリースのうちで、予定しているオプションのすべてがサポートされるように大きく進歩する予定です。

### ダウンロード <!-- Downloads -->
<!--
The release tarballs can be found on our [download page](/lxd/downloads).
-->
このリリースの tarball は [ダウンロードページ](/lxd/downloads) から取得できます。


## LXD 0.4 リリースのお知らせ <!-- LXD 0.4 release announcement --><span class="text-muted">2015 年 3 月 17 日 <!-- 17th of March 2015 --></span>

<!--
The major changes for this release are:
-->
このリリースの主な変更点は以下の通りです。

 * リモートにあるイメージからのコンテナの起動がサポートされました <!-- Support for starting a container from a remote image -->
 * ホスト間のコンテナのコピー／移動がサポートされました <!-- Support for copying/moving containers between hosts -->
 * コマンドラインが改良されました (リスト、エイリアス、プロファイル、短いハッシュ、など) <!-- Improved command line (listing, aliases, profiles, partial hashes, ...) -->
 * エラーログが改良されました <!-- Improved error logging -->
 * 仕様によりきっちり合うように API が修正されました <!-- API fixes to more closely match the spec -->
 * 多数のバグフィックス <!-- A lot of bugfixes -->

<!--
Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)
-->
このリリースはまだ LXD 開発の初期であり、現時点の LXD はまだプロダクション用途向きではないことに注意してください。そしてサポートはありません。(報告されたバグ修正やパッチは次のリリースに含まれる予定です)

<!--
At this point, most core LXD features are present but many of the  
particular options aren't implemented yet (don't match our  
specifications), we expect to make great progress in supporting all of  
the expected options over the next couple of releases.
-->
現時点で、ほとんどの LXD の機能の主要なものが提供されるようになりました。しかし、まだ多数の特定のオプションが実装されていません (仕様と一致していません)。今後の数リリースのうちで、予定しているオプションのすべてがサポートされるように大きく進歩する予定です。

### Downloads
<!--
The release tarballs can be found on our [download page](/lxd/downloads).
-->
このリリースの tarball は [ダウンロードページ](/lxd/downloads) から取得できます。


## LXD 0.3 リリースのお知らせ <!-- LXD 0.3 release announcement --><span class="text-muted">2015 年 3 月 10 日 <!-- 10th of March 2015 --></span>

<!--
The major changes for this release are:
-->
このリリースでの主な変更点は以下の通りです。

 * lxd:
    * exec を作りなおしました。インタラクティブモードとノン・インタラクティブモードを分離し、エスケープシーケンスを適切にサポートするようになりました <!-- Reworked exec, now with separate interactive and non-interactive modes and proper support for escape sequences. -->
    * イメージの取り扱いを改良しました。新たに圧縮アルゴリズムを追加し、イメージのエクスポートをサポートしました <!-- Improved image handling, now supporting more compression algorithms and support for image export. -->
    * ライブマイグレーションの初期サポート (特別な設定をコンテナに行う必要があります) <!-- Initial support of live migration (requires particular container configuration) -->
    * コンテナの設定とプロファイルの初期サポート <!-- Initial support of container configuration and profiles -->
        * ディスクとネットワークインターフェースのサポート <!-- Support for disks and network interfaces -->
        * プロファイルの作成・削除・割り当てのサポート <!-- Support for creating/deleting/assigining profiles -->
    * 特に指定されない限り全ての新しいコンテナに適用される "default" プロファイルを導入しました <!-- Introduce a "default" profile which is applied to all new containers unless otherwise specified. -->

* lxc:
    * 色々な "list" コマンドのユーザ体験の改良を行いました <!-- Improved user experience for the various "list" commands -->
    * info コマンドを改良しました。PID と IP アドレスが表示されるようになりました <!-- Improved info command, now showing PID and IP addresses -->
    * image info コマンドを実装しました。イメージのプロパティとエイリアスを表示します <!-- Implement the image info command, shows all image properties and aliases. -->
    * LXD に対する翻訳例として、初期の部分的なフランス語翻訳を行いました <!-- Early (partial) french translation as an example translation of LXD. -->
    * イメージとプロファイルに対する "edit" コマンドをサポートしました <!-- Support of the "edit" command for images and profiles. -->
 * lxd-images:
    * 最小の busybox イメージの作成をサポートするようになりました <!-- Now supports creating a minimal busybox image. -->
    * images.linuxcontainers.org からイメージをインポートする際の広範囲に対する改良を行いました。もう再パッケージングは不要です。 <!-- Vastly improved image imports from images.linuxcontainers.org by no longer requiring repacking. -->
    * Python 3.2 でも動作するようになりました <!-- Now working with python3.2 -->
 * テストスイート <!-- Testsuite -->:
    * コンテナの設定、プロファイル、デバイス、マイグレーション、コマンド実行(exec)、データベースに対するテストを追加しました <!-- Added tests for container configuration, profiles, devices, migration, exec and database. -->
    * 最小の busybox イメージを実行して、数秒で実行するようになりました <!-- Now running using a minimal busybox image, making it run in just a few seconds. -->
 * 多数のバグフィックスを行いました <!-- Many bugfixes -->

<!--
Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)
-->
このリリースはまだ LXD 開発の初期であり、現時点の LXD はまだプロダクション用途向きではないことに注意してください。そしてサポートはありません。(報告されたバグ修正やパッチは次のリリースに含まれる予定です)

<!--
At this point, most core LXD features are present but many of the  
particular options aren't implemented yet (don't match our  
specifications), we expect to make great progress in supporting all of  
the expected options over the next couple of releases.
-->
現時点で、ほとんどの LXD の機能の主要なものが提供されるようになりました。しかし、まだ多数の特定のオプションが実装されていません (仕様と一致していません)。今後の数リリースのうちで、予定しているオプションのすべてがサポートされるように大きく進歩する予定です。

### ダウンロード <!-- Downloads -->
<!--
The release tarballs can be found on our [download page](/lxd/downloads).
-->
このリリースの tarball は [ダウンロードページ](/lxd/downloads) から取得できます。


## LXD 0.2 リリースのお知らせ <!-- LXD 0.2 release announcement --><span class="text-muted">2015 年 2 月 27 日 <!-- 27th of February 2015 --></span>

<!--
The major changes for this release are:
-->
このリリースでの主な変更点は以下の通りです。

 * ビルトインイメージストアの最初のバージョン <!-- Initial version of the built-in image store -->
   * 全てのコンテナはイメージから作らなければならなくなりました <!-- All containers must now be created from images -->
   * イメージは提供の "lxd-images" ツールを使って LXD にインポートできます <!-- Images can be imported into LXD by using the provided "lxd-images" tool -->
   * イメージを見つけやすくするためのイメージのエイリアスを設定できます <!-- Image aliases can be setup to make it easier to find your images -->
 * データベースバックエンド (全ての LXD データは SQLite のデータベースに保存されるようになりました) <!-- Database backend (all LXD data is now stored in a SQLite database) -->
 * コンテナ設定の初期段階 (APIの一部のみ) <!-- Early stage of container configuration (partial API only) -->
 * gcc-go 経由の多数のアーキテクチャ向けのビルドのサポート (全ての依存関係に互換性があるとは限りません) <!-- Support for building for many architectures through gcc-go (not all dependencies are compatible) -->
 * exec のメカニズムの再構築 <!-- Reworked exec mechanism -->
 * 多数のバグフィックス <!-- A lot of bugfixes -->

<!--
Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)
-->
このリリースはまだ LXD 開発の初期であり、現時点の LXD はまだプロダクション用途向きではないことに注意してください。そしてサポートはありません。(報告されたバグ修正やパッチは次のリリースに含まれる予定です)

<!--
We are still busy working on container migration, proper container configuration and a stable REST API.
-->
我々はまだコンテナのマイグレーション、適切にコンテナを設定できるようにすること、stable な REST API の開発に精力的に取り組んでいます。

### ダウンロード <!-- Downloads -->
<!--
The release tarballs can be found on our [download page](/lxd/downloads).
-->
このリリースの tarball は [ダウンロードページ](/lxd/downloads) から取得できます。

## LXD 0.1 リリースのお知らせ <!-- LXD 0.1 release announcement --><span class="text-muted">2015 年 2 月 13 日 <!-- 13th of February 2015 --></span>

<!--
This is the initial LXD release.
-->
これは LXD の初めてのリリースです。

<!--
With this first release of LXD, it is possible to:
-->
この LXD の初めてのリリースでは、以下が可能です。

 * コンテナの一覧<!-- List containers -->
 * Ubuntu 14.04 LTS amd64 コンテナに対する create、destroy、start、stop、execute コマンドの実行 <!-- create, destroy, start, stop and execute commands into an Ubuntu 14.04 LTS amd64 container -->
 * コンテナの外と中の間でのファイルの転送 <!-- Transfer files in and out of containers -->
 * lxc コマンドラインツールを使った複数の LXD ホストの管理 <!-- Management of multiple LXD hosts through the lxc command line tool -->
 * LXD [REST API](/lxd/rest-api) の試験的な使用<!-- Experiment with the LXD REST API -->

<!--
Support for other container images, container migration, container configuration and profiles  
and a stable REST API will be coming in the next few releases.
-->
他のコンテナイメージ、コンテナマイグレーション、コンテナの設定とプロファイル、Stable な REST API はこの後のリリースで提供予定です。

<!--
This release is our first development snapshot and isn't intended for production use  
and comes with no support statement from upstream. 
(reported bugs and patches will be included in the next release)
-->
このリリースは最初の開発スナップショットであり、プロダクション用途向きではなく、サポートもありません。(報告されたバグ修正やパッチは次のリリースに含まれる予定です)

### ダウンロード <!-- Downloads -->
<!--
The release tarballs can be found on our [download page](/lxd/downloads).
-->

このリリースの tarball は [ダウンロードページ](/lxd/downloads) から取得できます。

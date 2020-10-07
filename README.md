# Awesome Web Archiving (ja) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

※この文書は、Creative Commons Zero v1.0 Universalライセンスで公開されている[iipc/awesome-web-archiving](https://github.com/iipc/awesome-web-archiving)を極めて適当に日本語に翻訳したものです。本文書は翻訳元文書と同じくCreative Commons Zero v1.0 Universalライセンスに従います。なお、翻訳元文書の性質上、ここに掲載されている文献やリンクは基本的に全て英語資料であることにご注意ください。  

----

Webアーカイブとは、World Wide Web(WWW)上に存在する情報を収集し、それを後世の研究者・歴史家、および公共のために「書庫(アーカイブ)」として記録する行為のことです。Webアーカイブを行う際は、保存対象であるWWWの情報が極めて厖大であるがゆえに、Webクローラを用いて自動的に情報を収集するのが一般的となっています。ウェブ標準は絶え間なく進化し続けており、それに伴ってWeb関連技術もまた変化し続けています。Webページを保存しアーカイブとして閲覧するという営みを、信頼でき有意義なものにするためには、Webアーカイブに用いられるソフトウェアもそうした技術発展に追随していかなくてはならないのです。

## 目次

* [入門ガイド](#trainingdocumentation)
* [Webコンテンツ著作者のための資料](#resources-for-web-publishers)
* [ツール・ソフトウェア](#tools--software)
  * [アーカイブの保存](#acquisition)
  * [アーカイブの閲覧・再生](#replay)
  * [情報の検索](#search--discovery)
  * [各種ユーティリティ](#utilities)
  * [WARC I/O Libraries](#warc-io-libraries)
  * [Analysis](#analysis)
  * [QA(品質保証)](#quality-assurance)
* [Webアーカイブコミュニティによる資料](#community-resources)
  * [このリスト以外の素晴らしいリスト](#other-awesome-lists)
  * [ブログ・学術研究](#blogs-and-scholarship)
  * [メーリングリスト](#mailing-lists)
  * [Slack](#slack)
  * [Twitter](#twitter)

## 入門ガイド

* Webアーカイブの考え方の手引き:
  * [What is a web archive?](https://youtu.be/ubDHY-ynWi0) - [the UK Web Archive のYouTubeチャンネル](https://www.youtube.com/channel/UCJukhTSw8VRj-VNTpBcqWkw)に投稿された動画
  * [Webアーカイブ・イニシアチブの一覧 (Wikipedia記事)](https://en.wikipedia.org/wiki/List_of_Web_archiving_initiatives)
  * [Glossary of Archive-It and Web Archiving Terms](https://support.archive-it.org/hc/en-us/articles/208111686-Glossary-of-Archive-It-and-Web-Archiving-Terms)
  * [The Web Archiving Lifecycle Model](https://archive-it.org/blog/post/announcing-the-web-archiving-life-cycle-model/) - Web Archiving Lifecycle Modelとは、Webアーカイブの技術的およびプログラム的な部分を、Webコンテンツをアーカイブしようとするあらゆる組織に関連するフレームワークに組み込もうとする取り組み。Archive-It (Internet ArchiveのWebアーカイブサービス) によって、同サービスと世界中の記憶機関(Memory Institutions)との協力関係を基にして確立されたもの。
  * [Training materials: module for beginners (8 sessions)](https://netpreserve.org/web-archiving/training-materials/)
* WARCファイルフォーマット標準について:
  * The [warc-specifications](https://iipc.github.io/warc-specifications/) community HTML version of the official specification and hub for new proposals.
  * The [offical ISO 28500 WARC specification homepage](http://bibnum.bnf.fr/WARC/).
* Webアーカイブを利用したい研究者のための手引き:
  * [GLAM Workbench: Web Archives](https://glam-workbench.github.io/web-archives/) - 関連記事：['Asking questions with web archives'](https://netpreserveblog.wordpress.com/2020/05/28/asking-questions-with-web-archives/).
  * [Archives Unleashed Toolkit documentation](https://aut.docs.archivesunleashed.org/)

## Webコンテンツ著作者のための資料

これらの資料は、Web上に情報を公開していて、なおかつ自分が公開した情報をアーカイブしたいと考えている個人・団体にとって参考になります。

* [Stanford Libraries' Archivability pages](https://library.stanford.edu/projects/web-archiving/archivability)
* [Archive Ready](http://archiveready.com/) - Webページがどの程度正しくアーカイブされそうか見積もってくれるツール


## ツール・ソフトウェア

ここで挙げているツールやソフトウェアのリストは、最も重要かつ広く使われているWebアーカイブ関連のツール類をざっと紹介することを目的としています。より詳しい情報を得たい場合、Webアーカイブに携わっている他の団体による以下の素晴らしい資料を参照 (ぜひ編集協力も！) することをお勧めします:
* [Comparison of web archiving software](https://github.com/archivers-space/research/tree/master/web_archiving)
* [Awesome Website Change Monitoring](https://github.com/edgi-govdata-archiving/awesome-website-change-monitoring)
* [Web Crawl @ COPTR](http://coptr.digipres.org/Category:Web_Crawl)

### アーカイブの保存

* [ArchiveBox](https://github.com/pirate/ArchiveBox) - A tool which maintains an additive archive from RSS feeds, bookmarks, and links using wget, chrome headless, and other methods (formerly `Bookmark Archiver`). *(In Development)* RSSフィード・ブックマーク・リンク集の情報をwget・ヘッドレスChromeなどを使ってアーカイブするツール。旧名称は`Bookmark Archiver`。 *(開発中)*
* [archivenow](https://github.com/oduwsdl/archivenow) - A [Python library](http://ws-dl.blogspot.com/2017/02/2017-02-22-archive-now-archivenow.html) to push web resources into on-demand web archives. *(Stable)*　[Pythonライブラリ](http://ws-dl.blogspot.com/2017/02/2017-02-22-archive-now-archivenow.html)。Web上のコンテンツをWebアーカイブサイト上に保存する。 *(安定版あり)*
* [Brozzler](https://github.com/internetarchive/brozzler) - A distributed web crawler (爬虫) that uses a real browser (chrome or chromium) to fetch pages and embedded urls and to extract links. *(Stable)*　分散型Webクローラ("爬虫")。Webブラウザ(Chrome/Chromium)を使い、Webサイトを埋め込みリンク・外部リンクも含めて保存する *(安定版あり)*
* [Chronicler](https://github.com/CGamesPlay/chronicler) - Web browser with record and replay functionality. *(In Development)* 記録・再生機能付きのWebブラウザ *(開発中)*
* [Crawl](https://git.autistici.org/ale/crawl) - A simple web crawler in Golang. *(Stable)* Golang製のシンプルなWebクローラ *(安定版あり)*
* [crocoite](https://github.com/promyloph/crocoite) - Crawl websites using headless Google Chrome/Chromium and save resources, static DOM snapshot and page screenshots to WARC files. *(In Development)* ヘッドレスChrome/Chromiumを用いてWebサイトをクロールし、コンテンツ・静的なDOMスナップショット・ページのスクリーンショットをWARCファイルとして保存するツール *(開発中)*
* [F(b)arc](https://github.com/justinlittman/fbarc) - A commandline tool and Python library for archiving data from [Facebook](https://www.facebook.com/) using the [Graph API](https://developers.facebook.com/docs/graph-api). *(Stable)* コマンドラインツール・Pythonライブラリ。Facebookの[Graph API](https://developers.facebook.com/docs/graph-api)を使ってFacebookのコンテンツをアーカイブする。 *(安定版あり)*
* [freeze-dry](https://github.com/WebMemex/freeze-dry) - JavaScript library to turn page into static, self-contained HTML document; useful for browser extensions. *(In Development)* *(開発中)*
* [grab-site](https://github.com/ArchiveTeam/grab-site) - The archivist's web crawler: WARC output, dashboard for all crawls, dynamic ignore patterns. *(Stable)* "WebアーキビストのためのWebクローラ"。WARC出力機能、実行中クロールを監視出来るダッシュボード機能、動的な無視パターンを搭載 *(安定版あり)*
* [Heritrix](https://github.com/internetarchive/heritrix3/wiki) - An open source, extensible, web-scale, archival quality web crawler. *(Stable)* オープンソース・高拡張性・Webスケール・アーカイバルクオリティなWebクローラ *(安定版あり)*
  * [Heritrix Walkthrough](https://github.com/web-archive-group/heritrix-walkthrough) *(In Development)* *(開発中)*
* [html2warc](https://github.com/steffenfritz/html2warc) - A simple script to convert offline data into a single WARC file. *(Stable)* オフラインのデータをWARCファイルに変換するためのシンプルなスクリプト *(安定版あり)*
* [HTTrack](http://www.httrack.com/) - An open source website copying utility. *(Stable)* オープンソースのWebサイトコピー用ユーティリティ *(安定版あり)*
* [monolith](https://github.com/Y2Z/monolith) - CLI tool to save a web page as a single HTML file. *(Stable)* WebページをHTMLファイルとして保存するCLIツール *(安定版あり)*
* [SingleFile](https://github.com/gildas-lormeau/SingleFile) - Browser extension for Firefox/Chrome and CLI tool to save a faithful copy of a complete page as a single HTML file. *(Stable)* Firefox/Chromeのブラウザ拡張機能・CLIツール。ページを丸ごと完全コピーしてHTMLファイルとして保存する *(安定版あり)*
* [SiteStory](http://mementoweb.github.com/SiteStory/) - A transactional archive that selectively captures and stores transactions that take place between a web client (browser) and a web server. *(Stable)* トランザクショナルアーカイブ。Webクライアント(=ブラウザ)とWebサーバの間のトランザクションを選択的にキャプチャし保存する。 *(安定版あり)*
* [Social Feed Manager](https://gwu-libraries.github.io/sfm-ui/) - Open source software that enables users to create social media collections from Twitter, Tumblr, Flickr, and Sina Weibo public APIs. *(Stable)* Twitter、Tumblr、Flickr、Weiboの公式APIを用いてソーシャルメディアの情報を収集するためのオープンソースソフトウェア。 *(安定版あり)*
* [Squidwarc](https://github.com/N0taN3rd/Squidwarc) - An [open source, high-fidelity, page interacting](http://ws-dl.blogspot.com/2017/07/2017-07-24-replacing-heritrix-with.html) archival crawler that uses Chrome or Chrome Headless directly. *(In Development)* [オープンソース・高忠実・ページインタラクティブ](http://ws-dl.blogspot.com/2017/07/2017-07-24-replacing-heritrix-with.html)なアーカイブ用クローラ。Chromeベース。 *(開発中)*
* [StormCrawler](http://stormcrawler.net/) - A collection of resources for building low-latency, scalable web crawlers on Apache Storm. *(Stable)* 低レイテンシでスケールするWebクローラを作るための各種コンポーネント。Apache Stormベース。 *(安定版あり)*
* [twarc](https://github.com/docnow/twarc) - A command line tool and Python library for archiving Twitter JSON data. *(Stable)* *(安定版あり)*
* [WARCreate](http://matkelly.com/warcreate/) - A [Google Chrome](https://www.google.com/intl/en/chrome/browser/) extension for archiving an individual webpage or website to a WARC file. *(Stable)* *(安定版あり)*
* [Warcworker](https://github.com/peterk/warcworker) - An open source, dockerized, queued, high fidelity web archiver based on Squidwarc with a simple web GUI. *(Stable)* *(安定版あり)*
* [WAIL](https://machawk1.github.io/wail/) - A graphical user interface (GUI) atop multiple web archiving tools intended to be used as an easy way for anyone to preserve and replay web pages; [Python](https://machawk1.github.io/wail/), [Electron](https://github.com/n0tan3rd/wail). *(Stable)* *(安定版あり)*
* [Web2Warc](https://github.com/helgeho/Web2Warc) - An easy-to-use and highly customizable crawler that enables anyone to create their own little Web archives (WARC/CDX). *(Stable)* *(安定版あり)*
* [WebMemex](https://github.com/WebMemex) - Browser extension for Firefox and Chrome which lets you archive web pages you visit. *(In Development)* *(開発中)*
* [Webrecorder](https://webrecorder.io/) - Create high-fidelity, interactive recordings of any web site you browse. *(Stable)* *(安定版あり)*
* [Wget](http://www.gnu.org/software/wget/) - An open source file retrieval utility that of [version 1.14 supports writing warcs](http://www.archiveteam.org/index.php?title=Wget_with_WARC_output). *(Stable)* *(安定版あり)*
* [Wget-lua](https://github.com/alard/wget-lua) - Wget with Lua extension. *(Stable)* *(安定版あり)*
* [Wpull](https://github.com/chfoo/wpull) - A Wget-compatible (or remake/clone/replacement/alternative) web downloader and crawler. *(Stable)* *(安定版あり)*

### アーカイブの閲覧・再生

* [InterPlanetary Wayback (ipwb)](https://github.com/oduwsdl/ipwb) - Web Archive (WARC) indexing and replay using [IPFS](https://ipfs.io/).
* [OpenWayback](https://github.com/iipc/openwayback/) - The open source project aimed to develop Wayback Machine, the key software used by web archives worldwide to play back archived websites in the user's browser. *(Stable)* *(安定版あり)*
* [PyWb](https://github.com/ikreymer/pywb) - A Python (2 and 3) implementation of web archival replay tools, sometimes also known as 'Wayback Machine'. *(Stable)* *(安定版あり)*
* [Reconstructive](https://oduwsdl.github.io/Reconstructive/) - Reconstructive is a ServiceWorker module for client-side reconstruction of composite mementos by rerouting resource requests to corresponding archived copies (JavaScript).
* [ReplayWeb.Page](https://replayweb.page/) - A browser-based, fully client-side replay engine for both local and remote WARC files.

### 情報の検索

* [Mink](https://github.com/machawk1/mink) - A [Google Chrome](https://www.google.com/intl/en/chrome/browser/) extension for querying Memento aggregators while browsing and integrating live-archived web navigation. *(Stable)* *(安定版あり)*
* [SecurityTrails](https://securitytrails.com/) - Web based archive for WHOIS and DNS records. REST API available free of charge. 
* [Tempas v1](http://tempas.L3S.de/v1) - Temporal web archive search based on [Delicious](https://en.wikipedia.org/wiki/Delicious_(website)) tags. *(Stable)* *(安定版あり)*
* [Tempas v2](http://tempas.L3S.de/v2) - Temporal web archive search based on links and anchor texts extracted from the German web from 1996 to 2013 (results are not limited to German pages, e.g., [Obama@2005-2009 in Tempas](http://tempas.l3s.de/v2/query?q=obama&from=2005&to=2009)). *(Stable)* *(安定版あり)*
* [webarchive-discovery](https://github.com/ukwa/webarchive-discovery) - WARC and ARC full-text indexing and discovery tools, with a number of associated tools capable of using the index shown below. *(Stable)* *(安定版あり)*
  * [Shine](https://github.com/ukwa/shine) - A prototype web archives exploration UI, developed with researchers as part of the [Big UK Domain Data for the Arts and Humanities project](https://buddah.projects.history.ac.uk/). *(Stable)* *(安定版あり)*
  * [SolrWayback](https://github.com/netarchivesuite/solrwayback) - A prototype web archives exploration UI with integrated playback functionality for WARCs. *(In Development)* *(開発中)*
  * [Warclight](https://github.com/archivesunleashed/warclight) - A Project Blacklight based Rails engine that supports the discovery of web archives held in the WARC and ARC formats. *(In Development)* *(開発中)*
  * [Wasp](https://github.com/webis-de/wasp) - A fully functional prototype of a personal [web archive and search system](http://ceur-ws.org/Vol-2167/paper6.pdf). *(In Development)* *(開発中)*
  * Other possible options for builting a front-end are listed on in the `webarchive-discovery` wiki, [here](https://github.com/ukwa/webarchive-discovery/wiki/Front-ends).

### 各種ユーティリティ

* [ArchiveTools](https://github.com/recrm/ArchiveTools) - Collection of tools to extract and interact with WARC files (Python).
* [har2warc](https://github.com/webrecorder/har2warc) - Convert HTTP Archive (HAR) -> Web Archive (WARC) format (Python).
* [httpreserve.info](http://httpreserve.info/) - Service to return the status of a web page or save it to the Internet Archive. Returns JSON via browser or command line via CURL using GET (Golang Package). *(Stable)* *(安定版あり)*
* [HTTPreserve Workbench](https://github.com/httpreserve/workbench) - Tool and API to describe the status of a web page encoded in a simple JSON output describing current status, and earliest and latest links on wayback.org. Save a web page to the Internet Archive. Audit lists of URIs and output a CSV with the data described above (Golang). *(In Development)*
* [MementoMap](https://github.com/oduwsdl/MementoMap) - A Tool to Summarize Web Archive Holdings (Python). *(In Development)* *(開発中)*
* [MemGator](https://github.com/oduwsdl/MemGator) - A Memento Aggregator CLI and Server (Golang). *(Stable)* *(安定版あり)*
* [node-cdxj](https://github.com/N0taN3rd/node-cdxj) - [CDXJ](https://github.com/oduwsdl/ORS/wiki/CDXJ) file parser (Node.js). *(Stable)* *(安定版あり)*
* [OutbackCDX](https://github.com/nla/outbackcdx) - RocksDB-based capture index (CDX) server supporting incremental updates and compression. Can be used as backend for OpenWayback, PyWb and [Heritrix](https://github.com/ukwa/ukwa-heritrix/blob/master/src/main/java/uk/bl/wap/modules/uriuniqfilters/OutbackCDXRecentlySeenUriUniqFilter.java). *(Stable)* *(安定版あり)*
* [py-wasapi-client](https://github.com/unt-libraries/py-wasapi-client) - Command line application to download crawls from WASAPI (Python). *(Stable)* *(安定版あり)*
* [The Archive Browser](https://archivebrowser.c3.cx/) - The Archive Browser is a program that lets you browse the contents of archives, as well as extract them. It will let you open files from inside archives, and lets you preview them using Quick Look. WARC is supported (macOS only, Proprietary app).
* [The Unarchiver](http://unarchiver.c3.cx/unarchiver) - Program to extract the contents of many archive formats, inclusive of WARC, to a file system. Free variant of The Archive Browser (macOS only, Proprietary app).
* [tikalinkextract](https://github.com/httpreserve/tikalinkextract) - Extract hyperlinks as a seed for web archiving from folders of document types that can be parsed by Apache Tika (Golang, Apache Tika Server). *(In Development)* *(開発中)*
* [wasapi-downloader](https://github.com/sul-dlss/wasapi-downloader) - Java command line application to download crawls from WASAPI. *(Stable)* *(安定版あり)*
* [WarcPartitioner](https://github.com/helgeho/WarcPartitioner) - Partition (W)ARC Files by MIME Type and Year. *(Stable)* *(安定版あり)*
* [webarchive-indexing](https://github.com/ikreymer/webarchive-indexing) - Tools for bulk indexing of WARC/ARC files on Hadoop, EMR or local file system.
* [wikiteam](https://github.com/WikiTeam/wikiteam) - Tools for downloading and preserving wikis. *(Stable)* *(安定版あり)*

### WARC I/O Libraries

* [HadoopConcatGz](https://github.com/helgeho/HadoopConcatGz) - A Splitable Hadoop InputFormat for Concatenated GZIP Files (and `*.warc.gz`). *(Stable)* *(安定版あり)*
* [jwarc](https://github.com/iipc/jwarc) - Reading and write WARC files with a typesafe API (Java).
* [Jwat](https://sbforge.org/display/JWAT/JWAT) - Libraries and tools for reading/writing/validating WARC/ARC/GZIP files (Java). *(Stable)* *(安定版あり)*
* [node-warc](https://github.com/N0taN3rd/node-warc) - Parse WARC files or create WARC files using either [Electron](https://electron.atom.io/) or [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) (Node.js). *(Stable)* *(安定版あり)*
* [Warcat](https://github.com/chfoo/warcat) - Tool and library for handling Web ARChive (WARC) files (Python). *(Stable)* *(安定版あり)*
* [warcio](https://github.com/webrecorder/warcio) - Streaming WARC/ARC library for fast web archive IO (Python).
* [warctools](https://github.com/internetarchive/warctools) - Library to work with ARC and WARC files (Python).
* [webarchive](https://github.com/richardlehane/webarchive) - Golang readers for ARC and WARC webarchive formats (Golang).

### Analysis

* [ArchiveSpark](https://github.com/helgeho/ArchiveSpark) - An Apache Spark framework (not only) for Web Archives that enables easy data processing, extraction as well as derivation. *(Stable)* *(安定版あり)*
* [Archives Unleashed Cloud](https://cloud.archivesunleashed.org) - Archives Unleashed Cloud (AUK) is an web interface for analysing web archives. Currently, it can sync with Archive-It collections and extract hyperlink networks, full text, and other information from your collections. *(Stable)* *(安定版あり)*
* [Archives Unleashed Notebooks](https://github.com/archivesunleashed/notebooks) - Notebooks for working with web archives with the Archives Unleashed Toolkit, and derivatives generated by the Archives Unleashed Toolkit. *(Stable)* *(安定版あり)*
* [Archives Unleashed Toolkit](https://github.com/archivesunleashed/aut) - Archives Unleashed Toolkit (AUT) is an open-source platform for analyzing web archives with Apache Spark. *(Stable)* *(安定版あり)*
* [Tweet Archvies Unleashed Toolkit](https://github.com/archivesunleashed/twut) - An open-source toolkit for analyzing line-oriented JSON Twitter archives with Apache Spark. *(In Development)* *(開発中)*

### QA(品質保証)

* [Chrome Check My Links](https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf) - Browser extension: a link checker with more options.
* [Chrome link checker](https://chrome.google.com/webstore/detail/link-checker/aibjbgmpmnidnmagaefhmcjhadpffaoi) - Browser extension: basic link checker.
* [Chrome link gopher](https://chrome.google.com/webstore/detail/bpjdkodgnbfalgghnbeggfbfjpcfamkf/publish-accepted?hl=en-US&gl=US) - Browser extension: link harvester on a page.
* [Chrome Open Multiple URLs](https://chrome.google.com/webstore/detail/open-multiple-urls/oifijhaokejakekmnjmphonojcfkpbbh?hl=de) - Browser extension: opens multiple URLs and also extracts URLs from text.
* [Chrome Revolver](https://chrome.google.com/webstore/detail/revolver-tabs/dlknooajieciikpedpldejhhijacnbda) - Browser extension: switches between browser tabs.
* [FlameShot](https://github.com/lupoDharkael/flameshot) - Screen capture and annotation on Ubuntu.
* [PlayOnLinux](https://www.playonlinux.com/en/) - For running Xenu and Notepad++ on Ubuntu.
* [PlayOnMac](https://www.playonmac.com/en/) - For running Xenu and Notepad++ on macOS.
* [Windows Snipping Tool](https://support.microsoft.com/en-gb/help/13776/windows-use-snipping-tool-to-capture-screenshots) - Windows built-in for partial screen capture and annotation. On macOS you can use Command + Shift + 4 (keyboard shortcut for taking partial screen capture).
* [WineBottler](http://winebottler.kronenberg.org/) - For running Xenu and Notepad++ on macOS.
* [xDoTool](https://github.com/jordansissel/xdotool) - Click automation on Ubuntu.
* [Xenu](http://home.snafu.de/tilman/xenulink.html) - Desktop link checker for Windows.


## Webアーカイブコミュニティによる資料

### このリスト以外の素晴らしいリスト

* [Web Archiving Community](https://github.com/pirate/ArchiveBox/wiki/Web-Archiving-Community)
* [Awesome Memento](https://github.com/machawk1/awesome-memento)
* [The WARC Ecosystem](http://www.archiveteam.org/index.php?title=The_WARC_Ecosystem)
* [The Web Crawl section of COPTR](http://coptr.digipres.org/Category:Web_Crawl)

### ブログ・学術研究

* [IIPC Blog](https://netpreserveblog.wordpress.com/)
* [Web Archiving Roundtable](https://webarchivingrt.wordpress.com/) - Unofficial blog of the Web Archiving Roundtable of the [Society of American Archivists](https://www2.archivists.org/) maintained by the members of the Web Archiving Roundtable.
* [The Web as History](http://www.ucl.ac.uk/ucl-press/browse-books/the-web-as-history) - An open-source book that provides a conceptual overview to web archiving research, as well as several case studies.
* [WS-DL Blog](https://ws-dl.blogspot.com/) - Web Science and Digital Libraries Research Group blogs about various Web archining related topics, scholarly work, and academic trip reports.
* [DSHR's Blog](https://blog.dshr.org/) - David Rosenthal regularly reviews and summarizes work done in the Digital Preservation field.
* [UK Web Archive Blog](https://blogs.bl.uk/webarchive/)

### メーリングリスト

* [IIPC](http://netpreserve.org/about-us/iipc-mailing-list/)
* [OpenWayback](https://groups.google.com/forum/#!forum/openwayback-dev)
* [WASAPI](https://groups.google.com/forum/#!forum/wasapi-community)

### Slack

* [IIPC Slack](https://iipc.slack.com/) - 参加を希望される方は [@netpreserve](https://twitter.com/NetPreserve) まで
* [Archives Unleashed Slack](https://archivesunleashed.slack.com/) - [Fill out this request form](https://docs.google.com/forms/d/e/1FAIpQLScXPIH0Ssw63yWqyMkUqHVYmz2-ItBMzHiJQ-sOlJwTA8u5AQ/viewform?usp=sf_link) for access to a researcher group of people working with web archives.
* [Archivers Slack](https://archivers.slack.com) - [Invite yourself](https://archivers-slack.herokuapp.com/) to a multi-disciplinary effort for archiving projects run in affiliation with [EDGI](https://envirodatagov.org/archiving/) and [Data Together](http://datatogether.org/).

### Twitter

* [@NetPreserve](https://twitter.com/NetPreserve) - IIPC公式アカウント
* [#WebArchiving](https://twitter.com/search?q=%23webarchiving)
* [#WebArchiveWednesday](https://twitter.com/hashtag/webarchivewednesday)

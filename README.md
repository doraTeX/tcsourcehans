tcsourcehans
============

upLaTeX で [Source Han Sans（源ノ角ゴシック）](http://blog.typekit.com/alternate/source-han-sans-jp/)を使うためのパッケージです。  
ZRさんの [tcsourcehans パッケージ](http://d.hatena.ne.jp/zrbabbler/20140719/1405795403) を縦書き対応に拡張したものです。

インストール法
-----
1. アーカイブを展開して出てくる各ディレクトリ・ファイルを，適切なディレクトリに移動させます。
  * `cmap/sourcehans` →  `$TEXMF/fonts/cmap/sourcehans`
  * `tfm/sourcehans` →  `$TEXMF/fonts/tfm/sourcehans`
  * `vf/sourcehans` →  `$TEXMF/fonts/vf/sourcehans`
  * `tcsourcehans.sty` → `$TEXMF/tex/latex/sourcehans/`

2. [GitHub のレポジトリ](https://github.com/adobe-fonts/source-han-sans/tree/release/SubsetOTF) から，`SourceHanSansJP.zip` をダウンロードし，展開して出てくる各フォントファイルを `$TEXMF/fonts/opentype/sourcehans/` に移動します。

3. 必要ならば `maketexlsr` を実行します。

使い方
-----
[ZRさんのオリジナルの tcsourcehans パッケージの使い方](http://d.hatena.ne.jp/zrbabbler/20140719/1405795403)
に準じます。

```
\usepackage{tcsourcehans}
```
としておけば，
```
\kanjifamily{sourcehans}
```
で和文ファミリが Source Han Sans に切り替わります。

シリーズとフォントのウェイトの対応は次の通り。
* el ↔ ExtraLight
* l ↔ Light
* m ↔ Normal
* mb ↔ Regular
* db ↔ Medium
* b / bx ↔ Bold
* eb ↔ Heavy

それゆえ，例えば
```
\kanjifamily{sourcehans}\fontseries{el}\selectfont
```
とすれば，和文フォントに SourceHanSansJP-ExtraLight.otf が使われるようになります。

使用例は，添付の test.tex や Gauche_the_Cellist.tex をご覧ください。

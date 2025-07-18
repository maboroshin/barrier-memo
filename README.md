
# キーボード/マウス共有ソフト

Windows/Mac/Linux間でマウスとキーボードを共有
* [barrier](https://github.com/debauchee/barrier)というソフトがあった。翻訳作業が難航だし、なかなか採用してくれないソフトだった。ともかく、管理者が不活発で、2021年のBarrier 2.4.0で終了？ 2024年に[input-leap](https://github.com/input-leap/input-leap/)に分裂した。

* 2025-06-14 [input-leap](https://github.com/input-leap/input-leap/releases) 3.0.3。Show all 16 assets からWindows用
* 2024-10-04 [input-leap 3.0.0](https://github.com/input-leap/input-leap/releases/tag/v3.0.0) 2.4.0用の日本語訳入ってる。

* 2024-10-02 Deskflow 1.17.0
 
* 2021-11-05 [日本語訳 #1375 2.4.0用](https://github.com/debauchee/barrier/pull/1375)
* 2021-11-02 [Barrier 2.4.0](https://github.com/debauchee/barrier/releases) やっと日本語訳が反映
* 2021-01-11 下記の日本語訳が採用される。かなり根本的に誤訳を直した。
* 2019-12-31 [日本語訳 #536 で改定](https://github.com/debauchee/barrier/pull/536)
* 2018-03-02 Barrier 2.0.0 RC1 (GitHubでの最初のリリース) Synergy 1.9から派生。

### Barrier 以前の Synergy

1996年に開発された Windows と Irix をつなぐ社内用 CosmoSynergy を、会社閉鎖後に2001年に Chris Schoenemanが書き直したのが Synergy。2006年まで Synergy 1.3.1。（参考: Wikipediaの [Synergy (software)](https://en.wikipedia.org/wiki/Synergy_(software))）元はSourceforgeにあったが、[synergy-vintage](https://github.com/nbolton/synergy-vintage)として公開されている。このビンテージによると、2009年にQtベースの1.3.5となり、[synergy-core](https://web.archive.org/web/20240807182632/https://github.com/symless/synergy-core)に移ったようだ。このコアのページはなくなった。徐々にバージョンアップ → [Uptodown](https://synergy.en.uptodown.com/windows/versions)

間はよくわからないけど、コアのソースコードを公開したまま、Synergy は商用製品として販売される。Synergy 1.9 が Barrier 2.0.0に派生した。BarrierなどはSynergyバージョン1のUIを継承しているようだ → [What is the difference between each version of Synergy?](https://help.symless.com/hc/en-us/articles/33562819211025-What-is-the-difference-between-each-version-of-Synergy)

* [Synergy](https://github.com/symless/synergy) 製品版のための安定版
* [Deskflow](https://github.com/deskflow/deskflow) : Synergyの開発者も参加する[完全なオープンソース](https://github.com/deskflow/deskflow/wiki/Relationship-with-Synergy)

### Barrierの翻訳メモ
* [Barrier翻訳法](https://github.com/debauchee/barrier/issues/1857)

Barrierの翻訳作業は、現在のところ以下の2ファイルをDiffで比較すればいい。

* src/gui/res/[lang](https://github.com/debauchee/barrier/tree/master/src/gui/res/lang)/ 翻訳ファイルがある。
* src/gui/[gui.ts](https://github.com/debauchee/barrier/blob/master/src/gui/gui.ts) 英語ファイルがある。

新しい翻訳文字列があればbarrierのtsファイル中に入れる。タスクトレイ内の右クリックの文字列のショートカットキーは、日本語用に独自に追加した。

* src/gui/[src](https://github.com/debauchee/barrier/tree/master/src/gui/src)/ sourceタグ部分のウインドウ構成のファイルがあり、新規文字列はここから確認できる。

* また本家 [synergy-core の翻訳サイト](https://crowdin.com/project/synergy-core)も同時に反映していく（ここも更新はない）。

#### tsファイル
tsファイル中の location タグはおそらくメモ用で実際には機能しておらず、sourceタグ部分が一致すれば、translation 部分を表示できるので、新しい文字列は勝手に追加していくとよい。

#### 翻訳の出典

Fixの翻訳: 「固定」なのか「修正」なのか

[synergyの構成ファイルのヘルプ](https://symless.com/help-articles/creating-text-config-files)より

> If Caps Lock acts strangely

とあり、訳すとこのようになる。

> Capsロックが奇妙にふるまうなら

それなら、このオプションをオンにしろということで「修正」のようだ。

``preserveFocus`` は、画面を切り替えてもフォーカスを維持するので「固定」にした。

----

Bump against の翻訳

``Bump against the screen edge with the mouse pointer twice in quick succession.`` は、

[ダブルタップの説明](https://github.com/debauchee/barrier/commit/03c1f06878ed1cf7bc34481a88333f7bef7a4c57#diff-afe9c21ac60108121c6391f76d5ef980aa2f8aceee9adfcb53e55b7fa1d247d1)とのこと。

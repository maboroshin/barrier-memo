# barrier-memo

[barrier](https://github.com/debauchee/barrier) の翻訳作業は、現在のところ以下の2ファイルをDiffで比較すればいい。

* ``src/gui/res/lang/`` 翻訳ファイルがある。
* ``src/gui/gui.ts`` 英語ファイルがある。

また本家 synergy-core の翻訳にも翻訳サイトから同時に反映していくし、新しい翻訳文字列があればbarrierのtsファイル中に入れる。タスクトレイ内の右クリックのショートカットは独自に追加した。

* ``src/gui/src`` sourceタグ部分のウインドウ構成のファイルがあり、新規文字列はここから確認できる。

## tsファイル
tsファイル中の location タグはおそらくメモ用で実際には機能しておらず、sourceタグ部分が一致すれば、translation 部分を表示できるので、新しい文字列は勝手に追加していくとよい。

## 翻訳の出典

### Fixの翻訳は、「固定」なのか「修正」なのか

[synergyの構成ファイルのヘルプ](https://symless.com/help-articles/creating-text-config-files)より

>If Caps Lock acts strangely

とあり、訳すとこのようになる。
>Capsロックが奇妙にふるまうなら

それなら、このオプションをオンにしろということで「修正」のようだ。

``preserveFocus`` は画面を切り替えてもフォーカスを維持するので「固定」にした。

### Bump against

``Bump against the screen edge with the mouse pointer twice in quick succession.`` は、

[ダブルタップの説明](https://github.com/debauchee/barrier/commit/03c1f06878ed1cf7bc34481a88333f7bef7a4c57#diff-afe9c21ac60108121c6391f76d5ef980aa2f8aceee9adfcb53e55b7fa1d247d1)とのこと。

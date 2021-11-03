# barrier-memo

[barrier](https://github.com/debauchee/barrier) の翻訳作業は、現在のところ以下の2ファイルをDiffで比較すればいい。

* ``src/gui/res/lang/`` 翻訳ファイルがある。
* ``src/gui/gui.ts`` 英語ファイルがある。

また本家 synergy-core の翻訳にも翻訳サイトから同時に反映していくし、新しい翻訳文字列があればbarrierのtsファイル中に入れる。タスクトレイ内の右クリックのショートカットは独自に追加した。

## tsファイル
tsファイル中の location タグはおそらくメモ用で実際には機能しておらず、sourceタグ部分が一致すれば、translation 部分を表示できるので、新しい文字列は勝手に追加していくとよい。

## 翻訳の出典

Fixの翻訳は、「固定」なのか「修正」なのか。

[synergyの構成ファイルのヘルプ](https://symless.com/help-articles/creating-text-config-files)より

>If Caps Lock acts strangely

とあり、訳すとこのようになる。
>Capsロックが奇妙にふるまうなら

それなら、このオプションをオンにしろということで「修正」のようだ。

``preserveFocus`` は画面を切り替えてもフォーカスを維持するので「固定」にした。

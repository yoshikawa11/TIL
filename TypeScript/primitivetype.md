## プリミティブ型
JavaScript のデータ型はプリミティブ型とオブジェクトに分かれる。プリミティブ型は次の通り

1. boolean型
1. number型
1. string型
1. undefined型：値が未定義であることを表す
1. null型：値がないことを表す
1. symbol型：一意で不変の型
1. bigint型：number型では表せない数値を扱える整数型

プリミティブ型の特徴
* イミュータブル：値を直接変更できない
* プロパティを持たない
  * `null`,`undefined`はプロパティを持たないが、文字列や数値型はプロパティを持ったオブジェクトとしても扱える。→オートボクシング

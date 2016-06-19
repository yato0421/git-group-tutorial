# GitとGitHubの講習会 グループ開発練習

## 概要
このリポジトリは平成28年度のGitとGitHubの講習会向けに作成しました。  
ひな形にプログラムを入力してもらう形式です。  
利用は自由です。

IDとパスワードの認証を別ファイルに分けて開発することで，グループ開発に必要な知識を学習します。

※変数の命名規則等については，適当なので知りません。＾＾  
※関数分けする意味についてはツッコまないでください。＾＾

## 構造
* login.c
  - 他ファイルの核となるプログラム
  - ここを変更せず，それ以外のファイルで開発すること
* input.c (input.h)
  * scan_id()
    - IDの入力を担う
    - 引数は無し
    - 戻り値は入力されたID
  * scan_pass()
    - パスワードの入力を担う
    - 引数は無し
    - 戻り値は入力されたパスワード
* auth.c (auth.h)
  * auth_id()
    - IDの認証を担う
    - 引数は入力されたID
    - 戻り値は正しいか正しくないか**(正しい:1 正しくない:0)**
  * auth_pass()
    - パスワードの認証を担う
    - 引数は入力されたパスワード
    - 戻り値は正しいか正しくないか**(正しい:1 正しくない:0)**
* output.c
  * print_result()
    - 認証結果の出力を担う
    - 引数はIDの認証結果, パスワードの認証結果
    - 戻り値は無し

## ライセンス
Copyright (c) 2016 [rikyuusima](https://github.com/rikyuusima)  
Released under the MIT license  
http://opensource.org/licenses/mit-license.php

# GitBookの種類について

GitBookの種類について以下に示す。



## websiteによる公開

作成したMarkdownコンテンツファイルをwebsiteに公開する。

公開するための方法については、大まかに以下の種類がある。

|  #   | GitBook作成方法                               | 公開URL                                      | データソース                                      | ブランチ    |
| :--: | --------------------------------------------- | -------------------------------------------- | ------------------------------------------------- | ----------- |
|  １  | ローカル編集後、GitBookクライアントでビルド   | <u>https://ユーザ名.github.io/doc-name/</u>  | <u>https://github.com/ユーザ名/doc-name/</u>      | master/docs |
|  ２  | ↑                                             | ↑                                            | ↑                                                 | gh-pages    |
|  ３  | <u>https://app.gitbook.com/</u>で編集したもの | <u>https://ユーザ名.gitbook.io/doc-name/</u> | <u>https://app.gitbook.com/ユーザ名/spaces</u> ※2 | -           |

※1 doc-name：リポジトリ名（ドキュメント名）

※2 設定により、さらにgithub.comへのリンクとなるが省略

本書では、上記#1の方法について記述するものである。



## ebookファイルによる出力

作成したMarkdownコンテンツファイルをpdf、epub、mobi形式ファイルとして出力する。

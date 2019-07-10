# プラグインのインストール

作成するGitBookに機能を追加するためのプラグインが、ノードモジュールとして用意されているので、必要に応じプラグインをインストールする。

ノードモジュールとは、Node.jsでnpmコマンドを使用してインストールすることで利用できる便利な機能が実装済みのモジュールである。

適用したいプラグインを「book.json」ファイルに記述し、インストールコマンドを実行することでインストールを行う。



## 適用プラグインの記述例

プロジェクト直下の「book.json」ファイルに適用したいプラグインを列挙する。

```json
{
    "title": "hoge User's Guide", 
    "description": "", 
    "language": "ja",
    "plugins": [							← pluginsセクション内に列挙する。
        "hide-published-with",                （カンマに注意-最後は付けないなど）
        "-sharing", 
        "-lunr", 
        "-search", 
        "search-pro-kui", 
        "expandable-chapters", 
        "theme-synerex"
    ],
  ：
  ：
}
```

NPM公式サイト（URL: [https://www.npmjs.com/ ](https://www.npmjs.com/ )）の各プラグイン詳細を参考に設定すること。



## プラグインのインストール

コマンドプロンプトで以下のコマンドを実行し、プラグインをインストールする。

```command
> gitbook install
```



## 推奨プラグイン

### Published with Gitbook を消す

デフォルト状態で表示されている Published with Gitbook を消したい場合、`hide-published-with` のプラグインを使用する。

```json
{
	"plugins": ["hide-published-with"],
}
```



### Twitter や Facebook などのアイコンを消す

デフォルト状態で表示されている SNS のシェアアイコンを消したい場合、プラグインで `-sharing` を指定する。

```json
{
	"plugins": ["-sharing"],
}
```

個別に表示・非表示を設定することも可能。

- [https://www.npmjs.com/package/gitbook-plugin-sharing](https://www.npmjs.com/package/gitbook-plugin-sharing)



### フォント、色テーマ変更アイコンを表示

フォント、色テーマを変更するためのアイコンを表示したい場合、プラグインで `-lunr` を指定する。

```json
{
	"plugins": ["-lunr"],
}
```



### 検索を無効にする

デフォルトで表示されている検索窓を消したい場合、プラグインで `-search` を指定する。

```json
{
	"plugins": ["-sharing"],
}
```



### 日本語での検索を可能にする

GitBook標準の検索機能では使いづらい、日本語検索を行いたい場合、プラグインで `search-pro-kui` を指定する。

```json
{
	"plugins": ["search-pro-kui"],
}
```



### チャプターごと折り畳み／展開を可能にする

チャプターごと折り畳み／展開を可能にしたい場合、プラグインで `expandable-chapters` を指定する。

```json
{
    plugins: ["expandable-chapters"]
}
```


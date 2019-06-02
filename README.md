# KivyアプリをAndroidのAPKに変換します

変換を依頼の方は以下の手順に従ってください。

## 手順

### 1. KivyLauncherで動作確認

このrepository内にあるKivyLauncherの20190602版を使ってAndroid端末上で十分に動作確認してください。この時ただ実行するのではなくlogにも何か出てないか確かめてください。

### 2. 見積もり

[E-mail](mailto:flow4re2c@gmail.com)か[Discord](https://discord.gg/B3qTkhP)にて必要な情報を送ってください。最低限必要なのは以下です。

- source codeへのlink(どのような形でも良いですがgithubやgitlab上のrepositoryだと助かります)
- もしproject内のfileに`buildozer.spec`が含まれていないのなら、packagingに最低限必要な以下の二つ
  - アプリの名前 (例: `My First App`)
  - アプリのpackage名 (例: `jp.gottadiveintopython.myfirstapp`)
- どのABIのKivyLauncherを使って動作確認したのか(例: `armeabi-v7a`)
- Google Play Storeで公開する為のrelease版のapkが要るか否か。8/1からはStoreで公開する為には複数のABI向けのapkを作らないといけないようなので、手間が増え、見積もり額も上がります。

一週間以内(暑い時は二週間以内)にはできるだけ見積もり額を伝えます。

料金はどんなに単純な物でも5000円(暫定)からで、私がsource codeを理解するのにどれだけの労力が必要かに依って増えます。なのでcode量が増えれば高くなりますし、同じcode量でも分りやすい説明があれば安くなると思います。

### 3. 支払い

私が示した金額に納得の場合は以下のいづれかの方法で支払ってください。

- Amazonギフト券(Eメールタイプ)
- PayPal

この時、あなたがどの依頼主なのか分かるようになっている方が良いです。例えばPayPalで払う場合は見積もりを頼んだ時のE-mail addressと同じE-mail addressのPayPal account、Amazonギフト券の場合はメッセージにて
見積もり時のE-mail addressを添えてくれれば 間違いが起きにくいと思います。

### 4. debug版のapkで動作確認

支払いが確認でき次第、一週間以内(暑い時は二週間以内)にはdebug版のapkを送るつもりです。送られてきたら動作確認をして、結果を教えてください。

### 5. release版のapkで動作確認(release版を依頼した人のみ)

その後**未署名**のrelease版を送るので、署名をして動作確認してください。

## debug版とrelease版の違い

- debug版
  - 署名無しで端末にinstallできる
  - Storeには多分上げられない
- release版
  - 署名しないと端末にinstallできない
  - Storeに上げられる

# あなた用に加工したKivyLauncherを作ります

加工の例

- あらかじめ日本語fontを組み込んでおく
- 別のversionのKivyを組み込んでおく
- よく使うmoduleを組み込んでおく(そうすれば各アプリ毎に用意する必要がなくなる)
  - (注意: どんなmoduleでも組み込めるわけではありません。例えば`numpy`, `opencv`, `ffpyplayer`等のような何らかのbuild作業が必要なmoduleの組み込みは**私は**今の所成功していません。)

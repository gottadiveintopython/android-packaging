# 基本情報

- Python 3.7.1
- Kivy v1.11.0
- 同梱されている非標準module
  - android
  - plyer
  - pyjnius
- `buildozer.spec`に書いた権限
  - INTERNET
  - READ_EXTERNAL_STORAGE
  - WRITE_EXTERNAL_STORAGE

# 3つapkがあるのは?

3種の[ABI](https://developer.android.com/ndk/guides/abis)向けのapkを作ったから。自分の端末に最適な物を選んだ方がサクサク動くと思われます。私の端末は`armeabi-v7a`にしか対応していないので他二つのapkは未testです。なので誰か動作確認してくれると嬉しいです。

- `armeabi-v7a` 32bit。多くの端末で動くと思われるが、32bit命令なので64bitCPUの性能を完全には活かせない可能性大。
- `arm64-v8a` 64bit。
- `x86_64` 64bit。

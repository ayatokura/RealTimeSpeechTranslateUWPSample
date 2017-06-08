# Universal Windows App - Speech Translation API デモ用サンプル

このデモの目的は、UWP audiograph ライブラリの使用方法を実証し、Microsoft Translator Speech Translation APIと統合することです。 このサンプルでは、オーディオ入力（例えばマイク）から入力し、翻訳されたテキストを音声出力（例：スピーカー）へ出力します。デモの内部的な流れは次のとおりです。

1. HttpClientを使用して、Speech Translation APIのサブスクリプションから秘密鍵を使用してAzure Cognitive Services 認証トークンを取得します。
2. ドロップダウンリストに [音声翻訳でサポートされている言語] (http://docs.microsofttranslator.com/languages.html) セットを入力します。
3. Websocketライブラリを使用して [Speech Translation API](http://docs.microsofttranslator.com/speech-translate.html) と通信します。
4. AudioGraphライブラリを接続し、Speech Translation APIへの入力のためにIEEE Float（AudioGraphからの出力）を16ビットPCMに変換する方法を示します。

## 準備について
Microsoft Visual Studio 2015 以降の開発環境が必要です。 Universal Windows App 開発するために必要な機能が有効になっていることを確認してください。

Microsoft Azure Cognitive Service で提供されるMicrosoft Translator [Speech Translation API](http://docs.microsofttranslator.com/speech-translate.html) を作成してください。

Azure開発ポータルでアクセスキーを取得します。 `MainPage.xaml.cs` にキーを入力してください:

```
const string AzureSecretKey = "[ここにAzureCognitiveServiceのTranslatorSpeechAPIのアクセスキーを入れる]";
```

## 参考
UWP Audiograph and Websocket references
- http://mtaulty.com/2016/02/09/windows-10-uwp-audiographrecording-microphone-to-wav-file/
- https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/AudioCreation
- https://msdn.microsoft.com/en-us/library/windows/apps/windows.media.audio.audiograph.aspx
- https://msdn.microsoft.com/en-us/windows/uwp/audio-video-camera/audio-graphs
- https://msdn.microsoft.com/en-us/windows/uwp/networking/websockets




# Washa

話者分離つきの AI 文字起こし。録音を「誰が・いつ・何を」に分けて文字にします。処理はすべて端末の中で行います。

AI transcription with speaker diarization. Washa turns a recording into who said what, and when — entirely on your device.

このリポジトリは配布物の置き場です(ソースコードは含みません)。/ This repository hosts downloads only (no source code).

> **ベータ版**: 2026-12-31 までお使いいただけます。/ **Beta**: usable until 2026-12-31.

## ダウンロード / Downloads

| OS | 入手 / How to get it |
|---|---|
| iPhone | TestFlight(招待制のベータ / invite-only beta) |
| Mac | TestFlight(招待制のベータ / invite-only beta) |
| Android | [Releases](https://github.com/Telepotch/washa-releases/releases) の APK / the APK in Releases |
| Windows | Microsoft Store(準備中 / coming soon) |

## 動作要件 / System requirements

| OS | 最低の版 / Minimum | CPU | 空き容量 / Free space |
|---|---|---|---|
| iPhone | iOS 26.0 | Apple シリコン | 1.0 GB |
| Mac | macOS 26.0 | Apple シリコン | 1.0 GB |
| Android | Android 13(API 33) | arm64-v8a | 1.4 GB |
| Windows | Windows 11 | x64 | 1.4 GB |

iPhone・Mac は、話者を聞き分けるデータと文字起こしの言語データを、初めて開いた時に Apple と Hugging Face から取得します。 / On iPhone and Mac, the speaker and speech data are downloaded from Apple and Hugging Face the first time you open Washa.

## Android・Windows が初回に取得するデータ / Data downloaded on first launch (Android and Windows)

固定のリリース [`models-2026-10-08`](https://github.com/Telepotch/washa-releases/releases/tag/models-2026-10-08) から取得します(中身は変えません)。 / Downloaded from the fixed release `models-2026-10-08` (never modified).

| ファイル / File | 大きさ / Size | 必須 / Required | ライセンス / License | SHA-256 |
|---|---|---|---|---|
| `sortformer-dynq8.onnx` | 141 MB | はい / yes | NVIDIA Open Model License Agreement | `68b909f197375f96221b8fa6dd3f8566a44dfd548a39f7f1a9505354d92b6e0a` |
| `wespeaker_trunk343.onnx` | 27 MB | はい / yes | CC BY 4.0 | `1abe2419c39571a48021f546c35218591caac63df905f92294357b9ef6ec203e` |
| `wespeaker_trunk343.q8.onnx` | 7 MB | 在れば使う / optional | CC BY 4.0 | `eb088639c84b7ba6a41653f19c35a2b28540ddd0dcf22d4e03bfb6b23f3b4d68` |
| `wespeaker_pool.bin` | 5 MB | はい / yes | CC BY 4.0 | `b29b833b47c18f53ba328fdb805799666e2a7b1576b80abd167fbfb9d37792e7` |
| `sense-voice-2024-07-17.int8.onnx` | 239 MB | はい / yes | FunASR Model Open Source License Agreement v1.1 | `c71f0ce00bec95b07744e116345e33d8cbbe08cef896382cf907bf4b51a2cd51` |
| `sense-voice-2024-07-17.tokens.txt` | 0 MB | はい / yes | FunASR Model Open Source License Agreement v1.1 | `f449eb28dc567533d7fa59be34e2abca8784f771850c78a47fb731a31429a1dc` |
| `silero_vad.onnx` | 1 MB | はい / yes | MIT | `9e2449e1087496d8d4caba907f23e0bd3f78d91fa552479bb9c23ac09cbb1fd6` |
| `pyannote-seg3.onnx` | 6 MB | 在れば使う / optional | MIT | `220ad67ca923bef2fa91f2390c786097bf305bceb5e261d4af67b38e938e1079` |

合計 / Total: 426 MB

各モデルのライセンス文と告知は [`LICENSES/`](LICENSES/) と [`LICENSES/MODELS-NOTICE.txt`](LICENSES/MODELS-NOTICE.txt) にあります。 / License texts and notices are in `LICENSES/`.

## リリースノート(build 15) / Release notes

- **はじめての案内**: 必要なデータの準備、Washa でできること、あなたの話者カードの作成を、順に案内します。
- **あなたの話者カード**: 短い文を 2 つ読み上げると、次の録音からあなたの名前で出てきます。設定からいつでも作り直せます。
- **保存場所**: Mac と Windows では、録音と話者台帳をホームの「washa」フォルダに置きます。設定から場所を変えられます。これまでのデータは自動で移します。
- **新しいアイコン**になりました。
- 人数を直した後の「話者台帳と比べています」の待ちを短くしました。
- このベータ版は 2026 年 12 月 31 日までお使いいただけます。

- **Getting started**: Washa now walks you through downloading what it needs, what it can do, and creating your speaker card.
- **Your speaker card**: Read two short passages aloud, and you'll appear by name in your next recordings. You can redo it any time in Settings.
- **Storage location**: On Mac and Windows, recordings and your speaker cards are kept in a "washa" folder in your home folder. You can change it in Settings. Your existing data moves there automatically.
- **New app icon.**
- Shorter wait for "Comparing with your speaker cards" after you change the number of people.
- This beta can be used until December 31, 2026.

---

© Teleport Inc. — [teleport.jp/washa](https://teleport.jp/washa/)

# AI Image Generator Skill

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

> 👉 こちらもどうぞ [AI Video Generator Skill](https://github.com/beatra-ai/ai-video-generator-skill)

商品画像、ブランドビジュアル、ポスター、SNS 画像、イラスト、写真のバリエーションを生成・合成・編集。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-image-generator-skill) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | 商品画像、ブランドビジュアル、ポスター、SNS画像、イラスト、写真のバリエーションを生成・合成・編集します。 |
| **モデル** | Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live、Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5 |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="夏の日差しの中で撮った架空のセージグリーン陶器製ハンドドリップセットの写真と、器具と配置はそのままに、ランプの灯る雪の冬の夜へ編集した同じ画像。Beatra AI で生成。"></p>

*夏の日差しの中で撮った架空のセージグリーン陶器製ハンドドリップセットの写真と、器具と配置はそのままに、ランプの灯る雪の冬の夜へ編集した同じ画像。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-image-generation-studio`](skills/ai-image-generation-studio) | [SKILL.md](skills/ai-image-generation-studio/SKILL.md) | 0.2.6 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-image-generation-studio) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/ai-image-generator-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/ai-image-generator-skill ai-image-generation-studio
```

または、このリポジトリをクローンして `skills/ai-image-generation-studio` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/ai-image-generator-skill から ai-image-generation-studio スキル（フォルダ skills/ai-image-generation-studio）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 作例

<p align="center"><img src="assets/demo-2.webp" width="800" alt="生成したハンドドリップセットを参照画像にした新しい構図：リネンの上に豆、ペーパーフィルター、真鍮のスプーンを並べた正方形の俯瞰フラットレイ。Beatra AI で生成。"></p>

*生成したハンドドリップセットを参照画像にした新しい構図：リネンの上に豆、ペーパーフィルター、真鍮のスプーンを並べた正方形の俯瞰フラットレイ。Beatra AI で生成。*

エージェントへの依頼例：

```text
./pourover-set.png を商品の参考画像にして、SNS 用の正方形の俯瞰フラットレイを作って：リネンの上にドリッパー、サーバー、コーヒーの入ったマグ、シュガーボウル、散らした豆、ペーパーフィルター、真鍮のスプーン。器の形と釉薬の色はわかるように残して。
```

プロンプト：

```text
New composition for a square social media post. Image 1 is the product reference: the sage-green ceramic pour-over dripper, the glass carafe, the sage-green mug and the speckled cream sugar bowl. Keep their shapes, glaze colors, speckled texture and proportions recognizable. Arrange them as a top-down overhead flat lay on a textured natural linen tablecloth: the dripper lying beside the carafe, the mug filled with black coffee seen from directly above, the sugar bowl, a small scattered line of whole coffee beans, a folded unbleached paper filter, and a brass coffee scoop. Soft even daylight from the upper left with gentle short shadows, calm balanced spacing between objects with breathing room around the edges, muted sage, cream, linen and warm brown palette, photoreal editorial product photography. No people, no hands, no text, no logos, no labels, no watermarks.
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **テキストから画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）／GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
- **画像から画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP
- **画像編集** — 6 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 4.2 MP
  - 4.2 MP（2K ティア）：Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP
- **画像から動画** — 9 モデル（Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）／480p〜4K／2〜30 秒／アスペクト比 16:9、1:1、21:9、3:4、4:3、9:16／MOV、MP4
  - 4K：Seedance 2.0、最長 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5、最高 1080p
  - ネイティブ音声：Wan 2.7、MiniMax H3

## 得られるもの

- **生成前に方向を決める** — 生成前に、伝えたい内容、被写体、構図、スタイル、光、色、用途、残したい要素を決めます。
- **重要な素材から始める** — 文章、順番を指定した1〜4枚の参考画像、1枚の元画像のいずれかを使い、選んだ方法から始めます。
- **次のバージョンの前に確認** — 生成された画像を確認してから、部分編集、再構成、再生成を1つ選びます。

## 活用シーン

- **商品画像を作る** — 手元の商品を新しいシーンに置くか、新しい商品コンセプトを生成し、形、色、ラベル、用途を確認します。
- **広告・ブランドビジュアルを作る** — 1つのメッセージ、配色、対象ユーザーから、広告画像やブランドビジュアルの案を作ります。
- **SNS画像とポスターを作る** — 掲載先、画像の向き、余白、メッセージに合わせて1枚を計画します。
- **イラストとコンセプトを作る** — 明確なビジュアルスタイルで、イラスト、表紙、シーン、コンセプト画像を検討します。
- **写真や背景を変更する** — 既存画像を元にして、物体、範囲、背景、全体の仕上がりのうち、変更したい点に焦点を当て、画像全体を確認します。
- **参考画像から新しい画像を作る** — 商品、被写体、スタイル、シーンの参考画像を順番に使って新しい画像を作り、どの特徴が反映されたか確認します。

## よくある質問

### 画像生成スタジオでは何が作れますか？

テキスト、参考画像、既存の元画像から、商品画像、広告クリエイティブ、ブランドビジュアル、ポスター、SNS画像、イラスト、コンセプトアート、写真のバリエーション、背景変更を作れます。

### 自分の写真や商品画像を使えますか？

はい。1〜4枚の画像を順番に使って新しい構図の参考にすることも、最初の画像を編集元として使うこともできます。生成された細部は確認が必要です。

### 画像の一部だけを変更できますか？

はい。既存の元画像で範囲を指定して部分編集し、被写体、構図、文字、用途の観点から画像全体も確認します。

### どの画像モデルを使いますか？

作りたい画像、参考素材、キャンバス、出力条件に合う現在のモデルを確認します。指定モデルが適合する場合はその選択を使い、適合する候補を明確にして制作方向を決めます。

### シリーズ画像の統一感を保てますか？

選んだ方向、文章、参考画像、被写体の特徴、スタイル、ロゴ位置、文字設計をシリーズで再利用し、各画像の統一感を確認します。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update ai-image-generation-studio` または
`gh skill update ai-image-generation-studio`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-image-generator-skill
- ドキュメント — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-image-generator-skill
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt （インデックス）· https://beatra.ai/llms-full.txt （全スキルを 1 ファイルに）

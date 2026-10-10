<p align="center">
  <img src="../../logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
  <strong align="center">ADHDに配慮した簡潔な出力。（診断済みかは関係なく、誰でも気軽に使えます！）</strong>
</p>
<p align="center">
  <a href="../../LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="ライセンス"></a>
</p>

<p align="center">
  <a href="../../README.md" title="English" aria-label="English">🇬🇧</a> ·
  <a href="README.zh-CN.md" title="简体中文" aria-label="简体中文">🇨🇳</a> ·
  <a href="README.id.md" title="Bahasa Indonesia" aria-label="Bahasa Indonesia">🇮🇩</a> ·
  <a href="README.pt-BR.md" title="Português (Brasil)" aria-label="Português (Brasil)">🇧🇷</a> ·
  <strong title="日本語" aria-label="日本語">🇯🇵</strong> ·
  <a href="README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
  <a href="README.ko.md" title="한국어" aria-label="한국어">🇰🇷</a> ·
  <a href="README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
  <a href="README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a> ·
  <a href="README.ar.md" title="العربية" aria-label="العربية">🇸🇦</a>
</p>

## インストール

CLIのプロンプトに以下をコピー＆ペーストしてください：

```text
Install the i-have-adhd skill/plugin from https://github.com/ayghri/i-have-adhd, refer to the repo's AGENTS.md for instructions.
```

または、🔗 [インストール手順を確認する](../install/INSTALL.ja.md)。

## 機能

コーディングアシスタントの回答を長文で埋めさせないようにするスキル。最優先は行動で、手順を箇条書きで整理。  「お役に立てれば幸いです！」などの不要な挨拶や定型文をカットします。

## 変化の例

<table>
<tr>
<td width="50%">

## 適用前

> 良い質問ですね！考えてみましょう。認証フローには、ミドルウェア、トークン検証、Cookieの処理といういくつかの要素があります。`src/auth.ts` を見ると、`verifyToken` 関数（42〜58行目付近）は古い `jsonwebtoken` API を使っているようです。一つの方法としては、パッケージを更新してその関数を書き直すことです。変更後は、認証テストを実行して問題が起きていないことを確認するとよいでしょう。ついでに、依存関係のバージョンも全体的に確認したほうがよいかもしれません。お役に立てれば幸いです！さらに詳しく調べたい場合はお知らせください。

</td>

<td width="50%">

## 適用後

> `src/auth.ts:42` のトークン検証を修正し、認証テストを実行しました。
>
> 検証済み：18件のテストが成功。古い依存関係は保留にしましたが、この修正を妨げません。

</td>
</tr>
</table>

## 動作方針

全文は [SKILL.md](../../skills/i-have-adhd/SKILL.md) を参照してください。

1. エージェントが安全に実行できる作業は、手順として返さず実行する。
2. 答え、結果、推奨案、またはブロッカーを最初に示す。
3. ユーザーが行う最初の一手を小さく具体的にする。
4. 表示する作業を「今・次・保留」に絞る。
5. 中断後は履歴全体を繰り返さず、必要な文脈だけを復元する。
6. 代替案を並べる前に、既定の推奨案を示す。
7. 検証済みの進捗、失敗、不明点を区別する。
8. 判断に役立つ場合だけ所要時間を見積もり、不確実性も示す。
9. 本当に必要な場合だけ、次の一手で終える。

## カスタマイズ

リポジトリをForkし、`skills/i-have-adhd/SKILL.md` を編集してから自分のコピーに差し替えます。

```bash
claude plugin uninstall i-have-adhd            # 先に本家のコピーを削除
claude plugin marketplace remove i-have-adhd   # Fork版と本家で名前が重複するため
claude plugin marketplace add <your-username>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Claude Code を再起動し、`/i-have-adhd` をもう一度呼び出してください。

## クレジット

J. Russell Ramsay と Anthony L. Rostain による著書『*The Adult ADHD Tool Kit*』に着想を得ています。人間の一日のスケジュール管理ではなく、LLMがどう返答すべきかに合わせて最適化しています。

## ライセンス

[MIT](../../LICENSE)

もし1回でも「良い質問ですね！」を読み飛ばすスクロールが減ったなら、Star⭐️をお願いします。

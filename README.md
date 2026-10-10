<p align="center">
  <img src="./logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
  <strong align="center">Less friction between “I know” and “it’s done.” No ADHD diagnosis needed.</strong>
</p>
<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="License"></a>
</p>

<p align="center">
  <strong title="English" aria-label="English">🇬🇧</strong> ·
  <a href=".github/readme/README.zh-CN.md" title="简体中文" aria-label="简体中文">🇨🇳</a> ·
  <a href=".github/readme/README.es.md" title="Español" aria-label="Español">🇪🇸</a> ·
  <a href=".github/readme/README.pt-BR.md" title="Português (Brasil)" aria-label="Português (Brasil)">🇧🇷</a> ·
  <a href=".github/readme/README.ja.md" title="日本語" aria-label="日本語">🇯🇵</a> ·
  <a href=".github/readme/README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
  <a href=".github/readme/README.ko.md" title="한국어" aria-label="한국어">🇰🇷</a> ·
  <a href=".github/readme/README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
  <a href=".github/readme/README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a> ·
  <a href=".github/readme/README.ar.md" title="العربية" aria-label="العربية">🇸🇦</a>
</p>


## Install

Copy/paste into your CLI prompt:

```text
Install the i-have-adhd skill/plugin from https://github.com/ayghri/i-have-adhd, refer to the repo's AGENTS.md for instructions.
```

Or 🔗 [check the installation instructions](INSTALL.md).

## What it does

A skill for coding assistants that helps with the parts after the answer: starting, choosing, resuming after an interruption, and finishing. When the assistant can safely do the work, it does the work instead of handing you a checklist.

It still cuts filler. It no longer treats every response as the same formatting problem.

[Kacper Rutkiewicz | AI Made Simple](https://youtu.be/NEl8kPWZP_Y) has made a good breakdown of an earlier version of the skill.

## What changes


<table>
<tr>
<td width="50%">

## Before

> Edit `src/auth.ts:42` to update token validation.
>
> 1. Open `src/auth.ts`
> 2. Replace `verifyToken`
> 3. Run `npm test -- auth.spec.ts`

</td>

<td width="50%">

## After

> Fixed token validation in `src/auth.ts:42` and ran the auth tests.
>
> Verified: 18 passed. The stale dependency is parked; it does not block this fix.

</td>
</tr>
</table>


## The behavior

Full text in [SKILL.md](./skills/i-have-adhd/SKILL.md).

1. Do agent-owned work instead of delegating it back.
2. Put the answer, result, recommendation, or blocker first.
3. Make the reader's required starting move concrete and small.
4. Keep one live working set: now, next, and parked.
5. Restore context after interruptions without replaying the whole history.
6. Recommend a default before listing alternatives.
7. Separate verified progress from failures and unknowns.
8. Estimate time only when it helps a decision, with honest uncertainty.
9. End with one next move only when a next move is actually needed.

## Tune it

Fork, edit `skills/i-have-adhd/SKILL.md`, then swap your copy in:

```bash
claude plugin uninstall i-have-adhd            # drop the upstream copy first:
claude plugin marketplace remove i-have-adhd   # fork and upstream share both names
claude plugin marketplace add <your-username>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Restart your coding assistant, then re-invoke `/i-have-adhd`.

## Credits

Loosely based on *The Adult ADHD Tool Kit* by J. Russell Ramsay and Anthony L. Rostain. Adapted for how an LLM should respond, not how a human should organize their day.

## License

[MIT](LICENSE).

Star ⭐ if it saved you one scroll past one "Great question!"

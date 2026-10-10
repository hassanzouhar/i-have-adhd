<p align="center">
  <img src="../../logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
  <strong align="center">ADHD 친화적인 출력. ADHD 진단은 필요 없어요!</strong>
</p>
<p align="center">
  <a href="../../LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="License"></a>
</p>

<p align="center">
  <a href="../../README.md" title="English" aria-label="English">🇬🇧</a> ·
  <a href="README.zh-CN.md" title="简体中文" aria-label="简体中文">🇨🇳</a> ·
  <a href="README.id.md" title="Bahasa Indonesia" aria-label="Bahasa Indonesia">🇮🇩</a> ·
  <a href="README.pt-BR.md" title="Português (Brasil)" aria-label="Português (Brasil)">🇧🇷</a> ·
  <a href="README.ja.md" title="日本語" aria-label="日本語">🇯🇵</a> ·
  <a href="README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
  <strong title="한국어" aria-label="한국어">🇰🇷</strong> ·
  <a href="README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
  <a href="README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a> ·
  <a href="README.ar.md" title="العربية" aria-label="العربية">🇸🇦</a>
</p>


## 설치

🔗 [설치 안내](../install/INSTALL.ko.md)

## 무슨 일을 하나

코딩 어시스턴트가 답을 긴 글 속에 묻어두지 못하게 막는 스킬입니다. **행동 우선**, 단계는 **번호로**, "도움이 되었기를!" 같은 군더더기 없음.


## 무엇이 달라지는가


<table>
<tr>
<td width="50%">

## 사용 전

> 좋은 질문이네요! 한번 생각해볼게요. 인증 흐름에는 미들웨어, 토큰 검증, 쿠키 처리 같은 여러 부분이 있어요. `src/auth.ts`를 살펴보면 `verifyToken` 함수(42~58번째 줄 근처)가 구버전 `jsonwebtoken` API를 쓰는 것 같아요. 한 가지 방법은 패키지를 업데이트하고 그 함수를 다시 작성하는 거예요. 변경 후에는 인증 테스트를 돌려서 문제가 없는지 확인해야 해요. 아, 그리고 하나 더, 전체 의존성 버전도 살펴보시면 좋을 것 같아요. 도움이 되었기를! 더 깊이 파고 싶으시면 알려주세요.

</td>

<td width="50%">

## 사용 후

> `src/auth.ts:42`의 토큰 검증을 수정하고 인증 테스트를 실행했습니다.
>
> 확인됨: 테스트 18개 통과. 오래된 의존성은 보류했으며 이번 수정에는 영향을 주지 않습니다.

</td>
</tr>
</table>


## 동작 방식

전문은 [SKILL.md](../../skills/i-have-adhd/SKILL.md)에 있습니다.

1. 에이전트가 안전하게 할 수 있는 일은 사용자에게 체크리스트로 돌리지 않고 직접 수행합니다.
2. 답, 결과, 추천 또는 막힌 지점을 먼저 보여 줍니다.
3. 사용자가 해야 하는 첫 행동을 작고 구체적으로 만듭니다.
4. 보이는 작업은 지금, 다음, 보류로 제한합니다.
5. 중단 후 전체 기록을 반복하지 않고 필요한 맥락만 복원합니다.
6. 대안을 나열하기 전에 기본 추천을 먼저 제시합니다.
7. 검증된 진행, 실패, 미확인 상태를 구분합니다.
8. 결정에 도움이 될 때만 시간을 추정하고 불확실성을 밝힙니다.
9. 실제로 필요한 경우에만 다음 행동 하나로 끝냅니다.

## 커스터마이즈

저장소를 포크해 `skills/i-have-adhd/SKILL.md`를 수정한 다음, 본인 복사본으로 교체하세요:

```bash
claude plugin uninstall i-have-adhd            # 먼저 업스트림 버전 제거
claude plugin marketplace remove i-have-adhd   # 포크와 업스트림이 같은 이름을 씁니다
claude plugin marketplace add <your-username>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Claude Code를 재시작한 뒤 `/i-have-adhd`를 다시 호출하세요.

## 크레딧

J. Russell Ramsay와 Anthony L. Rostain의 *The Adult ADHD Tool Kit*을 느슨하게 참고했습니다. 사람이 하루를 어떻게 꾸려야 하는가가 아니라 **LLM이 어떻게 응답해야 하는가**에 맞춰 재해석했습니다.

## 라이선스

[MIT](../../LICENSE).

"좋은 질문이네요!" 없는 답변을 한 번이라도 받았다면 Star ⭐ 부탁드립니다.

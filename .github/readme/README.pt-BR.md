<p align="center">
  <img src="../../logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
  <strong align="center">Respostas amigáveis para quem tem TDAH. Sem precisar de diagnóstico!</strong>
</p>
<p align="center">
  <a href="../../LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="Licença"></a>
</p>

<p align="center">
  <a href="../../README.md" title="English" aria-label="English">🇬🇧</a> ·
  <a href="README.zh-CN.md" title="简体中文" aria-label="简体中文">🇨🇳</a> ·
  <a href="README.id.md" title="Bahasa Indonesia" aria-label="Bahasa Indonesia">🇮🇩</a> ·
  <strong title="Português (Brasil)" aria-label="Português (Brasil)">🇧🇷</strong> ·
  <a href="README.ja.md" title="日本語" aria-label="日本語">🇯🇵</a> ·
  <a href="README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
  <a href="README.ko.md" title="한국어" aria-label="한국어">🇰🇷</a> ·
  <a href="README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
  <a href="README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a> ·
  <a href="README.ar.md" title="العربية" aria-label="العربية">🇸🇦</a>
</p>


## Instalação

🔗 [Instruções de instalação](../install/INSTALL.pt-BR.md)

## O que ela faz

Uma skill para o seu assistente de código que impede que ele enterre a resposta. Ação primeiro. Passos numerados. Nada de "Espero ter ajudado!"


## O que muda


<table>
<tr>
<td width="50%">

## Antes

> Ótima pergunta! Deixa eu pensar sobre isso. Seu fluxo de autenticação tem algumas partes envolvidas: o middleware, a verificação do token e o tratamento do cookie. Olhando o `src/auth.ts`, a função `verifyToken` (por volta das linhas 42-58) parece estar usando uma API antiga do `jsonwebtoken`. Uma abordagem seria atualizar o pacote e reescrever essa função. Depois da mudança, você vai querer rodar os testes de autenticação para confirmar que nada quebrou. Aliás, talvez valha a pena revisar as versões das suas dependências no geral. Espero ter ajudado! Me avise se quiser se aprofundar.

</td>

<td width="50%">

## Depois

> Corrigi a validação do token em `src/auth.ts:42` e rodei os testes de autenticação.
>
> Verificado: 18 testes passaram. A dependência desatualizada ficou estacionada; ela não bloqueia esta correção.

</td>
</tr>
</table>


## O comportamento

Texto completo no [SKILL.md](../../skills/i-have-adhd/SKILL.md).

1. Faça o trabalho que cabe ao agente em vez de devolvê-lo ao usuário.
2. Coloque primeiro a resposta, o resultado, a recomendação ou o bloqueio.
3. Torne a primeira ação exigida do usuário pequena e concreta.
4. Mantenha um único conjunto de trabalho visível: agora, próximo e estacionado.
5. Restaure o contexto após interrupções sem repetir todo o histórico.
6. Recomende uma opção padrão antes de listar alternativas.
7. Separe progresso verificado de falhas e desconhecidos.
8. Estime o tempo só quando isso ajudar uma decisão, mostrando a incerteza.
9. Termine com um próximo passo apenas quando ele for realmente necessário.

## Personalize

Faça um fork, edite `skills/i-have-adhd/SKILL.md` e troque pela sua cópia:

```bash
claude plugin uninstall i-have-adhd            # remova a cópia do upstream primeiro:
claude plugin marketplace remove i-have-adhd   # fork e upstream compartilham o mesmo nome
claude plugin marketplace add <seu-usuario>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Reinicie o Claude Code e invoque `/i-have-adhd` de novo.

## Créditos

Baseado livremente em *The Adult ADHD Tool Kit*, de J. Russell Ramsay e Anthony L. Rostain. Adaptado para como um LLM deveria responder, não para como uma pessoa deveria organizar o dia.

## Licença

[MIT](../../LICENSE).

Dê uma ⭐ se isso te poupou de rolar a tela por mais um "Ótima pergunta!"

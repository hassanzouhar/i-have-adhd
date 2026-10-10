<p align="center">
  <img src="../../logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
  <strong align="center">Respuestas adaptadas para TDAH. ¡No se necesita diagnóstico de TDAH!</strong>
</p>
<p align="center">
  <a href="../../LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="License"></a>
</p>

<p align="center">
  <a href="../../README.md" title="English" aria-label="English">🇬🇧</a> ·
  <a href="README.zh-CN.md" title="简体中文" aria-label="简体中文">🇨🇳</a> ·
  <strong title="Español" aria-label="Español">🇪🇸</strong> ·
  <a href="README.pt-BR.md" title="Português (Brasil)" aria-label="Português (Brasil)">🇧🇷</a> ·
  <a href="README.ja.md" title="日本語" aria-label="日本語">🇯🇵</a> ·
  <a href="README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
  <a href="README.ko.md" title="한국어" aria-label="한국어">🇰🇷</a> ·
  <a href="README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
  <a href="README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a>
</p>


## Instalación

Copia/pega en tu línea de comandos:

```text
Install the i-have-adhd skill/plugin from https://github.com/ayghri/i-have-adhd, refer to the repo's AGENTS.md for instructions.
```

O 🔗 [consulta las instrucciones de instalación](../../INSTALL.md).

## Qué hace

Una *skill* que reduce la fricción entre entender y terminar: ayuda a empezar, elegir, retomar tras una interrupción y cerrar el trabajo. Si el asistente puede hacer la tarea de forma segura, la hace en lugar de devolverte una lista de instrucciones.


## Qué cambia


<table>
<tr>
<td width="50%">

## Antes

> ¡Excelente pregunta! Déjame pensarlo. Tu flujo de autenticación tiene varias piezas móviles: el middleware, la verificación del token y el manejo de cookies. Mirando `src/auth.ts`, la función `verifyToken` (alrededor de las líneas 42-58) parece estar usando una API antigua de `jsonwebtoken`. Un enfoque sería actualizar el paquete y reescribir esa función. Después de hacer el cambio, tendrás que ejecutar las pruebas de autenticación para confirmar que nada se rompa. Por cierto, también deberías revisar las versiones de tus dependencias en general. ¡Espero que esto ayude! Avísame si quieres profundizar más.

</td>

<td width="50%">

## Después

> Corregí la validación del token en `src/auth.ts:42` y ejecuté las pruebas de autenticación.
>
> Verificado: 18 pruebas aprobadas. La dependencia desactualizada queda aparcada; no bloquea esta corrección.

</td>
</tr>
</table>


## El comportamiento

Texto completo en [SKILL.md](../../skills/i-have-adhd/SKILL.md).

1. Haz el trabajo que le corresponde al agente en vez de devolvérselo al usuario.
2. Pon primero la respuesta, el resultado, la recomendación o el bloqueo.
3. Haz que el primer paso requerido del usuario sea pequeño y concreto.
4. Mantén un único conjunto de trabajo visible: ahora, después y aparcado.
5. Restaura el contexto tras interrupciones sin repetir todo el historial.
6. Recomienda una opción por defecto antes de mostrar alternativas.
7. Separa el progreso verificado de los fallos y lo desconocido.
8. Estima el tiempo solo si ayuda a decidir y muestra la incertidumbre.
9. Termina con un siguiente paso solo cuando realmente haga falta.

## Ajustarlo

Haz un fork, edita `skills/i-have-adhd/SKILL.md`, luego intercambia tu copia:

```bash
claude plugin uninstall i-have-adhd            # elimina la copia original primero:
claude plugin marketplace remove i-have-adhd   # el fork y el original comparten ambos nombres
claude plugin marketplace add <tu-usuario>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Reinicia tu asistente de código y vuelve a invocar `/i-have-adhd`.

## Créditos

Basado libremente en *The Adult ADHD Tool Kit* de J. Russell Ramsay y Anthony L. Rostain. Adaptado para cómo un LLM debería responder, no para cómo un humano debería organizar su día.

## Licencia

[MIT](../../LICENSE).

Dale una estrella ⭐ si te ahorró hacer scroll ignorando un "¡Excelente pregunta!"

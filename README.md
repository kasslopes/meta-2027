# Desafio Meta 2027 — app local (PWA)

App de desafio de economia com 200 depósitos crescentes. Roda 100% no celular,
sem servidor, offline e com os dados salvos no próprio aparelho — mesma técnica do openGym.

## Arquivos
- `index.html` — o app inteiro (interface + lógica)
- `manifest.json` — identidade do app (nome, ícone, tela cheia)
- `sw.js` — service worker (cache offline)
- `icons/` — ícones 192 e 512

## Como testar rápido
Abra o `index.html` no navegador do celular. Já funciona. Mas pra virar
"app instalável" e offline de verdade, ele precisa ser servido por HTTPS
(abrir o arquivo direto com file:// não ativa o service worker).

## Publicar igual openGym (GitHub Pages) — grátis e instalável
1. Crie um repositório no GitHub (ex: `meta-2027`).
2. Suba estes arquivos mantendo a estrutura (`index.html`, `manifest.json`, `sw.js`, `icons/`).
3. No repositório: **Settings → Pages → Branch: main / root → Save**.
4. Em ~1 min sai um link tipo `https://seu-usuario.github.io/meta-2027/`.
5. Abra esse link no celular → menu do navegador → **"Adicionar à tela inicial"**.
   Pronto: vira ícone, abre em tela cheia e funciona offline.

## Como usar
1. Digite a meta e toque em **Aplicar** (recalcula os 200 valores).
2. Para registrar: digite o valor do depósito, anexe a foto do comprovante e
   toque em **Registrar e abater depósitos**.
3. O valor abate os depósitos **a partir do centro** da grade, indo pra fora.
   O que sobrar fica no **Caixa** e entra no próximo registro.
4. Dá pra marcar/desmarcar depósitos manualmente tocando na grade.
5. **Exportar backup** salva um `.json` com tudo.

Dados ficam só no seu celular. Limpar os dados do navegador apaga o progresso —
use o backup.

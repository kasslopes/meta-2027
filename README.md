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

## Três métodos em paralelo (abas no topo)
A mesma meta vale para os três; cada um tem seu próprio progresso e caixa.
- **Tabela** — 200 depósitos crescentes que somam a meta; comprovante abate a partir do centro da grade.
- **Primo Rico (ARCA)** — meta dividida em 4 caixinhas (Ações, Fundos imobiliários, Caixa, Internacional, ~25% cada, 10–40%); cada depósito é distribuído entre elas. Inclui a Regra dos 300 (gasto mensal × 300) para calcular a meta.
- **Sardinha** — aporte constante: define-se o nº de meses e aporta-se o mesmo valor por mês até a meta.

> Adaptações de poupança inspiradas na filosofia pública de cada autor. Não é recomendação de investimento nem produto oficial deles.

## Como usar
1. Defina a meta na engrenagem (⚙️) — ela vale para os 3 métodos; dá para configurar ARCA e Sardinha ali também, todos juntos.
2. Navegue entre os métodos pelas **abas** no topo.
3. Para registrar: digite o valor, anexe a foto e toque em **Registrar neste método** — o depósito entra no método da aba ativa; a sobra fica no **Caixa** daquele método.
4. Dá pra marcar/desmarcar manualmente tocando na grade/meses.
5. **Exportar backup** salva um `.json`; **Zerar tudo** apaga meta, progresso dos 3 métodos e comprovantes.

Dados ficam só no seu celular. Limpar os dados do navegador apaga o progresso —
use o backup.

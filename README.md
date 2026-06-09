# Sortudão — Front Duplo (Edição Diego Rox)

Landing page de pré-venda com **front duplo** (R$ 19,90 / R$ 29,90) que joga o lead
direto na **2ª tela do checkout** Sortudão (dados pessoais) com a quantidade de chances
**pré-selecionada** — estratégia para subir o ticket médio reduzindo o atrito de escolha.

**No ar:** https://hxcorp2025.github.io/sortudao-front-duplo/

## Como funciona o redirecionamento
Cada botão aponta para a rota `/compra` do checkout com o parâmetro `q` (nº de chances):

| Pacote | Chances | Link | Valor (R$ 0,49/chance) |
|---|---|---|---|
| 1 | 40 | `…/compra?pdv_code=d7066o&q=40` | ~R$ 19,60 (4 raspadinhas) |
| 2 | 60 | `…/compra?pdv_code=d7066o&q=60` | ~R$ 29,40 (6 raspadinhas) |

> A rota `/compra` exige `?q=` (ou `?combo=`/`?up=`) para liberar entrada direta — senão
> o checkout redireciona para a home. Com `q`, ela monta no passo *informar-dados-pessoais*.

### Cravar R$ 19,90 / R$ 29,90 no centavo (produção)
O checkout cobra R$ 0,49 × chance, então `q` gera múltiplos de 0,49. Para cravar valores
exatos, criar 2 ofertas no painel Sortudão/Play55 e trocar os `href` pelos links oficiais
(ou usar o parâmetro `up` com `offerId` real). Links centralizados no topo do `index.html`.

## Stack
HTML + CSS artesanal (sem framework). Fontes Inter + Lato. Assets reais da campanha.
Hospedado em GitHub Pages.

## Status
**v1** — conceito para apresentação interna. Copy baseada nas transcrições reais dos
criativos do Diego Rox ("valoriza o mínimo", risco de R$ 0,49, raspe e ganhe na hora).

# joelhosemdor.online

Página de vendas do **Protocolo Joelho sem dor**, de Raí Alves (@raialves.treinador).
Coprodução SB Business OS.

## v5: o produto mudou (12/09/26)

Até a v4 a página vendia **9 módulos organizados por região da dor**. No vídeo de
estratégia de 12/09/26 o produto foi reduzido a **um protocolo de 7 dias com um
objetivo só: desinflamar**. Os motivos:

- Um módulo para cada dor cria expectativa de resolver menisco e ligamento, e cada
  caso é um caso.
- Entregar o tratamento inteiro tira o motivo de a pessoa procurar o acompanhamento.

A página inteira foi reescrita em cima disso. A espinha dorsal deixou de ser "onde dói"
e passou a ser **a ordem: desinflamar, depois fortalecer, depois voltar ao que você gosta**.
O produto é o passo 1, e a página diz isso abertamente.

**A novidade da oferta é a consulta do dia 7:** uma consulta individual com o Raí, que
avulsa custa R$ 49,90, inclusa para quem compra. Ela é o bônus e é a ponte para o
acompanhamento.

## Como funciona

Página única, sem build e sem dependência de framework. As imagens vivem em `img/`
como `.webp`, com `loading="lazy"`. As fontes (Archivo, Karla, IBM Plex Mono) vêm do
Google Fonts.

| Arquivo | Para que serve |
|---|---|
| `index.html` | A landing page inteira (HTML + CSS + JS) |
| `img/rai.webp` | Foto oficial do Raí, no bloco "Quem vai te guiar" |
| `img/rai-avatar.webp` | Recorte quadrado do rosto, usado no mockup do WhatsApp |
| `img/depo-1..4.webp`, `img/comentario.webp` | Prova social recortada do perfil |
| `img/og.jpg` | Preview de compartilhamento (WhatsApp, 1200x630) |
| `CNAME` | Domínio custom do GitHub Pages (`joelhosemdor.online`) |

### Imagens que saíram de uso

`img/mod-01..09.webp` e `img/banner.webp` **não são mais referenciados**. Eles mostram
os 9 módulos que saíram do produto e trazem o nome antigo "PRIMEIRO DEGRAU" impresso na
arte. Os arquivos continuam no repositório, sem uso na página. O mockup da área de
membros passou a ser feito em CSS puro, sem imagem.

## Estrutura da página

Hero (cartão dos 7 dias) · tira de prova · checklist de reconhecimento · 5 verdades e
escala de dor · a ordem em 3 passos · zona segura · os 7 dias, dia a dia · a sequência
de WhatsApp · para quem é e para quem não basta · o presente do dia 7 · área de membros ·
quem é o Raí · depoimentos · oferta · ponte para o acompanhamento · FAQ · fechamento.

## Origem do arquivo

O arquivo de trabalho fica no Mac, em
`10. Parceiros Coproduçao/Raí Alves Joelho sem dor/PrimeiroDegrau-LP.html`.
O `index.html` daqui é esse mesmo arquivo com o bloco de comentário interno removido,
porque este repositório é público e o código-fonte fica visível para qualquer visitante.

Ao atualizar a página, edite o arquivo de trabalho no Mac, remova o comentário interno
de novo e sobrescreva o `index.html`.

## Pendências da página

1. `[REVISAO]` o Raí precisa assinar o conteúdo dos 7 dias antes de a página ir ao ar.
   Ele é o responsável técnico.
2. `[CONSULTA]` confirmar o valor avulso da consulta (R$ 49,90) e quantos horários por
   semana ele reserva para quem vem do protocolo.
3. `[GARANTIA]` a garantia de 7 dias vence no mesmo dia em que a consulta é entregue.
   Hoje dá para receber a consulta e pedir reembolso. Subir a garantia para 14 ou 30
   dias resolve.
4. `[WHATSAPP]` a página promete uma sequência diária no WhatsApp que ainda não existe.
   Roteiro pronto em `../Automacao WhatsApp 7 Dias/roteiro-7-dias.md`.
5. `[OG]` `img/og.jpg` ainda traz o nome antigo e a promessa dos 9 módulos.
6. `[PIXEL]` pixel da Meta e GA4 ainda não instalados (ponto marcado no fim do arquivo).
7. `[HISTORIA]` falta a história de origem do Raí no bloco "Quem vai te guiar".

As imagens de prova social saíram de publicações públicas do perfil do Raí. Falta
confirmar a autorização dos alunos que aparecem nelas.

## Checkout

Os botões de compra apontam para **https://pay.kiwify.com.br/S9zYTd8** (Kiwify).
R$ 97,00 à vista, ou até 12x de R$ 10,03, com Cartão, Boleto e Pix. A seção da oferta
mantém o `id="checkout"`.

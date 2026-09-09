# joelhosemdor.online

Página de vendas do **Primeiro Degrau**, de Raí Alves (@raialves.treinador).
Coprodução SB Business OS.

## Como funciona

Página única, sem build e sem dependência de framework. A partir da v4 as imagens
**não são mais base64 embutido**: elas vivem em `img/` como `.webp`, carregadas
com `loading="lazy"`. O `index.html` caiu de 205 KB para ~80 KB e as imagens
somam ~740 KB carregadas sob demanda, contra os ~20 MB dos PNGs originais.
As fontes (Archivo, Karla, IBM Plex Mono) vêm do Google Fonts.

| Arquivo | Para que serve |
|---|---|
| `index.html` | A landing page inteira (HTML + CSS + JS) |
| `img/mod-01..09.webp` | As 9 capas oficiais dos módulos |
| `img/rai.webp` | Foto oficial do Raí, usada no bloco "Quem vai te guiar" |
| `img/rai-avatar.webp` | Recorte quadrado do rosto. Não usado hoje, guardado para reuso |
| `img/banner.webp` | Banner da área de membros, usado no mockup de tela |
| `img/depo-1..4.webp`, `img/comentario.webp` | Prova social recortada do perfil |
| `img/og.jpg` | Preview de compartilhamento (WhatsApp, 1200x630) |
| `CNAME` | Domínio custom do GitHub Pages (`joelhosemdor.online`) |

## Estrutura da página

A v4 foi reorganizada em torno das capas dos módulos. A espinha dorsal deixou de
ser o diagnóstico e passou a ser **a região onde dói**, que é como a pessoa
realmente chega. A tabela "seu diagnóstico vira um módulo" existe para quem já
tem laudo na mão.

Hero (deck de capas) · tira de prova · os 9 módulos · 3 guias de situação ·
mapa diagnóstico para módulo · checklist de identificação · 5 verdades + escala
de dor · zona segura · plano de 21 dias · área de membros · quem é o Raí ·
depoimentos · oferta · ponte para o acompanhamento · FAQ · fechamento.

## Origem do arquivo

O arquivo de trabalho fica no Mac, em
`10. Parceiros Coproduçao/Raí Alves Joelho sem dor/PrimeiroDegrau-LP.html`.
O `index.html` daqui é esse mesmo arquivo com o bloco de comentário interno
removido, porque este repositório é público e o código-fonte da página fica
visível para qualquer visitante.

Ao atualizar a página, edite o arquivo de trabalho no Mac, remova o comentário
interno de novo e sobrescreva o `index.html`.

Para regerar as imagens a partir das capas originais em `Area de membros/`:

```sh
cwebp -q 80 -resize 760 0 -m 6 -sharp_yuv "01 oficial.png" -o img/mod-01.webp
```

## Pendências da página

1. `[CHECKOUT]` os 4 botões de compra ainda apontam para `#checkout`, não para o
   link real da Cakto
2. `[HISTORIA]` falta a história de origem do Raí no bloco "Quem vai te guiar"
3. `[GARANTIA]` os 7 dias são o mínimo do CDC art. 49, falta o Raí confirmar
4. `[PIXEL]` pixel da Meta e GA4 ainda não instalados (o ponto de inserção está
   marcado no fim do `index.html`)
5. `[LEGENDAS]` as descrições dos 9 módulos foram escritas a partir do título de
   cada capa. O Raí precisa confirmar se batem com o conteúdo real
6. `[MAPA]` a tabela "diagnóstico para módulo" segue a correspondência anatômica
   usual (condromalácia na frente, banda iliotibial fora, e assim por diante).
   Confirmar com o Raí antes de publicar
7. `[SITUACOES]` os 3 guias de situação (musculação, emagrecimento, teste
   físico) vieram da v3. Confirmar se existem mesmo no material
8. `[5CAUSAS]` confirmar quais são as 5 causas do modelo dele

As imagens de prova social saíram de publicações públicas do perfil do Raí.
Falta confirmar a autorização dos alunos que aparecem nelas.

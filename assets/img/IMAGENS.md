# Imagens do site — o que entrou e como

Convertidas em 15/08/2026 com ffmpeg, a partir dos originais em
`clientes/OdontologiaCaldasCoelho/Fotos e Imagens/` (pasta fora do git).

| Arquivo | Origem | Corte / tratamento |
|---|---|---|
| `fachada-topo.webp` 1230×915 | `ChatGPT Image 27 de ago. de 2026, 15_15_37.png` | `crop=1230:915:0:170`. Hero no desktop, e também o card da seção "O consultório". O corte em 1230 tira a placa lateral do quadro |
| `fachada-topo-mobile.webp` 620×1085 | a mesma imagem | `crop=620:1085:510:0` — recorte de retrato centrado no letreiro, que a 620 de largura ocupa 94% do quadro com 3% de folga de cada lado. Calçada e rua embaixo (onde o texto mora), prédio e céu em cima (onde a barra fica) |
| `atendimento.webp` 1400×854 | `ScreenShot_20260815182317.png` | **`crop=1263:770:0:0` — corta a paciente inteira fora do quadro.** Ver a regra abaixo |
| `dupla.webp` 500×500 | `fdafafadme.png` | sem corte |
| `dra-mariana.webp` 800×1000 | `ScreenShot_20260815173303.png` | `crop=608:760:120:0` pra 4:5 |
| `dr-paulo.webp` 800×1000 | `fdafafadme.png` | `crop=300:375:200:0` — recortado da foto dos dois, porque não veio retrato dele sozinho |
| `favicon.svg` | desenhado | logo do infinito em SVG, com o degradê verde→bege |

## O que ainda falta

- **`dra-fe.webp`** — não veio nenhuma foto da Dra. Fe Santos. O card dela
  mostra o bege com as iniciais "FS", que é um estado honesto, não um defeito.

## O que NÃO pode entrar no site

Duas das imagens enviadas são **"antes e depois"** e ficaram de fora:

- `ScreenShot_20260815182534.png` — gengivoplastia, antes e depois
- `ScreenShot_20260815182609.png` — profilaxia em fumante, antes e depois

O Código de Ética Odontológica veda divulgação de "antes e depois" como
publicidade, **mesmo com autorização do paciente**. Ela publica isso no
Instagram dela, e isso é escolha dela; o que sai com a assinatura do Marcelo
não vai. Não reintroduzir "porque ela mesma já postou".

## Regras que valem mais que a qualidade da foto

1. **A foto de atendimento entrou com a paciente cortada fora do quadro.** Não
   é só direito de imagem: é dado de saúde, e o sigilo é da paciente. Foi por
   isso que o véu escuro da faixa pôde ser aliviado — **não há ninguém a
   proteger no quadro**. Se a imagem for trocada por outra com paciente,
   escurecer não resolve: véu se remove abrindo o arquivo, corte não.
2. **As fotos de estúdio são da fotógrafa Soraia Reis** — a assinatura está
   visível nas imagens e foi mantida de propósito. O direito autoral é dela.
   Antes de publicar de verdade, confirmar com a Mariana se o uso em site está
   liberado.

## As imagens do topo são geradas por IA — o que aprendemos com elas

O usuário trouxe duas em 27/08/2026, ambas reconstruções da fachada real, com
qualidade bem melhor que o print que estava no ar. **A que ficou é a
`15_15_37`** (plano fechado). As duas substituíram `fachada.webp` e
`fachada-mobile.webp`, que foram pra `Fotos e Imagens/fachada-antiga/`.

**Por que a `15_58_58` (plano aberto) foi descartada.** Ela chegou a ficar no ar
por uma hora e resolvia bem o enquadramento, mas **a placa lateral saiu
destruída**: o infinito virou um nó, "Paulo Coelho" virou "Paulo Cuolho",
"Mariana Caldas" virou "Marleno Cotlas", os registros viraram rabisco e os dois
telefones ficaram embaralhados. Palavras do usuário: *"a placa está muito ruim e
bugada, no pc dá pra ver claramente e isso pode ser um ponto negativo"*. Ela
segue em `Fotos e Imagens/` caso um dia sirva pra outra coisa — **não usar em
nada onde a placa apareça.**

**Na `15_15_37` a placa está limpa e correta** — lê-se "ODONTOLOGIA / Paulo
Coelho CRO 26573 / Mariana Caldas CRO 26572", que bate com o que o usuário
conferiu no site do conselho. Mesmo assim ela fica **fora do quadro** no recorte
do desktop (o corte para em 1230 e ela começa em 1245): no tamanho em que
apareceria no hero ela é ilegível, e placa ilegível no canto é ruído, não
credencial. O registro dos dois já está escrito no rodapé, que é onde o Código
de Ética Odontológica exige.

⚠️ **A regra que sobrevive a tudo isso: texto dentro de imagem gerada por IA é
suspeito até ser conferido na fonte.** Duas imagens do mesmo prompt, no mesmo
dia, e uma delas escreveu o nome do dentista errado.

⚠️ **MEDIR COM `ffprobe`, NÃO COM `System.Drawing`.** O `[System.Drawing.Image]`
do PowerShell devolve o tamanho ajustado por DPI — pra `15_15_37` ele diz
1448×1086, e o tamanho real em pixels é **1408×1085**. Uma rodada inteira de
recorte foi perdida por causa disso: com a medida errada o letreiro parecia
ocupar 50% da largura, o que tornava impossível um recorte de retrato; medido
certo ele ocupa 41%, e o retrato sai sem esforço. `ffprobe -v error
-show_entries stream=width,height -of csv=p=0 <arquivo>`.

## Se aparecerem originais melhores

`dupla.webp` tem só 500×500 e é a mais fraca do conjunto. Se ela mandar as
originais da câmera, é só reconverter com os mesmos nomes.

# Imagens do site — o que entrou e como

Convertidas em 15/08/2026 com ffmpeg, a partir dos originais em
`clientes/OdontologiaCaldasCoelho/Fotos e Imagens/` (pasta fora do git).

| Arquivo | Origem | Corte / tratamento |
|---|---|---|
| `fachada-topo.webp` 1250×916 | `ChatGPT Image 27 de ago. de 2026, 15_15_37.png` | `crop=1250:916:0:170`. Hero no desktop, e também o card da seção "O consultório" |
| `fachada-topo-mobile.webp` 830×1086 | a mesma imagem | `crop=830:1086:400:0` — recorte vertical centrado no letreiro, que a 830 de largura ocupa 88% do quadro |
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

## A imagem do topo é gerada por IA — e isso tem uma consequência

`ChatGPT Image 27 de ago. de 2026, 15_15_37.png` foi trazida pelo usuário em
27/08/2026: é a fachada real reconstruída com qualidade bem melhor que o print
que estava no ar. Substituiu `fachada.webp` e `fachada-mobile.webp`, que foram
pra `Fotos e Imagens/fachada-antiga/`.

⚠️ **O recorte do desktop corta a placa lateral do canto direito de propósito,
e não é decisão estética.** A IA reconstruiu aquela placa com os registros
**inventados**:

- "**CPO** 26573" pro Dr. Paulo — não existe "CPO", o conselho é o CRO
- "CRO 26**S**72" pra Dra. Mariana — o real é **26572**, e o "5" virou "S"

Na foto original esses números estão ilegíveis, então não há de onde conferir.
Número de conselho errado em site de dentista é assunto de CRO, não de design —
o Código de Ética Odontológica manda o registro estar correto e visível. Os
`crop` acima resolvem na origem, tirando a placa do quadro.

**Se a imagem do topo for trocada um dia, conferir se a placa voltou ao quadro
antes de publicar.** E vale a regra geral: em imagem gerada por IA, todo texto
que aparece dentro dela é suspeito até ser conferido contra a fonte real.

## Se aparecerem originais melhores

`dupla.webp` tem só 500×500 e é a mais fraca do conjunto. Se ela mandar as
originais da câmera, é só reconverter com os mesmos nomes.

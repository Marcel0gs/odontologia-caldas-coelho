# Imagens do site — o que entrou e como

Convertidas em 15/08/2026 com ffmpeg, a partir dos originais em
`clientes/OdontologiaCaldasCoelho/Fotos e Imagens/` (pasta fora do git).

| Arquivo | Origem | Corte / tratamento |
|---|---|---|
| `fachada.webp` 1600×1186 | `ScreenShot_20260815182259.png` | escalado pra 1600 (lanczos). Hero no desktop |
| `fachada-mobile.webp` 820×1244 | `ScreenShot_20260815182347.png` | `crop=580:880:230:45` — a foto larga recortada em vertical. Pega a fachada inteira com a placa legível, o que a foto de perto não consegue num quadro vertical |
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

## Se aparecerem originais melhores

`fachada.webp` veio de um print de 1259px de largura e foi escalado pra 1600 —
funciona sob o degradê do hero, mas o arquivo original da câmera renderia
melhor em tela grande. `dupla.webp` tem só 500×500 e é a mais fraca do
conjunto. Se ela mandar as originais, é só reconverter com os mesmos nomes.

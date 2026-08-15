# Ícones das especialidades

Sete dos oito estão no site. **Falta `endodontia.png`** — nenhum dos arquivos
enviados representava canal ou raiz, então esse card ainda mostra o glifo verde
de reserva. É o único que destoa dos outros sete.

## Mapeamento — o que virou o quê

| Arquivo no site | Original em `Fotos e Imagens/Icones/` |
|---|---|
| `periodontia.png` | `seguro-dental.png` (dente com escudo) |
| `implantodontia.png` | `implantar.png` |
| `ortodontia.png` | `dente (1).png` (dente com bracket) |
| `ofm.png` | `maxilar.png` (arcada) |
| `dentistica.png` | `dente.png` (dente com brilhos) |
| `odontopediatria.png` | `dentista.png` (personagem) |
| `harmonizacao.png` | `perfil.png` (rosto com seringa) |
| **`endodontia.png`** | **falta** — precisa de um ícone de canal / raiz |

Sobrou sem uso: `aparelho-ortodontico.png`, redundante com o que foi pra
ortodontia.

**Trocar de ideia é barato:** é só reconverter por cima, com o mesmo nome. O
site não precisa de nenhuma alteração.

## Como o site desenha

O círculo é o **sálvia-claro da marca**, e o desenho entra dentro dele a 74% do
tamanho — não é o PNG que faz o círculo. Isso resolveu duas coisas de uma vez:
os arquivos vieram com fundo transparente (não como círculo cheio, como no
exemplo de referência), e a paleta da marca acabou segurando os oito cards em
vez de oito cores fortes brigando entre si.

**Consequência prática:** ícone novo pode vir com fundo transparente à vontade.
O que não pode é vir com fundo colorido próprio — ficaria círculo dentro de
círculo.

## Formato

- Quadrado, 512×512 nos originais. O site consome a 176×176, gerado por
  ffmpeg com `format=rgba` + `pad` pra fechar o quadrado (o `perfil.png` veio
  512×571 e precisou disso).
- PNG com alpha. SVG também serve e pesa menos — se vier, é só trocar a
  extensão nas regras `.card__ico--*` do `style.css`.

## Onde ficam os originais

`Fotos e Imagens/Icones/` (fora do git). Só os convertidos, com os nomes da
tabela, ficam aqui — esta pasta **é** versionada, porque é ela que o site
consome.

# Ícones das especialidades

Os oito estão no site.

## Mapeamento — o que virou o quê

| Arquivo no site | Original em `Fotos e Imagens/Icones/` |
|---|---|
| `periodontia.png` | `seguro-dental.png` (dente com escudo) |
| `implantodontia.png` | `implantar.png` |
| `endodontia.png` | `pngtree-endodontics-…jpg` — **ver a nota abaixo** |
| `ortodontia.png` | `dente (1).png` (dente com bracket) |
| `ofm.png` | `maxilar.png` (arcada) |
| `dentistica.png` | `dente.png` (dente com brilhos) |
| `odontopediatria.png` | `dentista.png` (personagem) |
| `harmonizacao.png` | `perfil.png` (rosto com seringa) |

Sobrou sem uso: `aparelho-ortodontico.png`, redundante com o que foi pra
ortodontia.

### A nota do ícone de endodontia

Esse veio em **JPG, com fundo branco sólido** — os outros sete vieram em PNG
com alpha. Fundo branco dentro de um círculo sálvia apareceria como um quadrado
branco, então o branco foi removido com `colorkey` no ffmpeg:

```
colorkey=0xFFFFFF:0.04:0.03
```

**Efeito colateral aceito:** o `colorkey` apaga *todo* branco da imagem, não só
o do fundo — então o miolo do dente, que era branco, ficou vazado e mostra o
sálvia por trás. Em 44px isso não se percebe: o que se lê é o contorno, a
gengiva rosa, a polpa amarela e o instrumento. **Se um dia esse ícone for usado
grande, o vazado aparece** e aí precisa do arquivo em PNG com alpha de verdade.

Lição pro próximo: **pedir sempre PNG ou SVG com fundo transparente.** JPG não
tem canal alpha, e recortar depois sempre custa alguma coisa.

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

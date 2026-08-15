# Ícones das especialidades

O site já está esperando estes oito arquivos. **Enquanto um deles não existe, o
card mostra o glifo verde sobre o círculo sálvia** — não quebra, não some, não
aparece imagem partida. Assim dá pra soltar os ícones um a um, conforme ficarem
prontos, sem mexer em código nenhum.

## Os nomes, exatos

| Arquivo | Card |
|---|---|
| `periodontia.png` | Periodontia |
| `implantodontia.png` | Implantodontia |
| `endodontia.png` | Endodontia |
| `ortodontia.png` | Ortodontia |
| `ofm.png` | Ortopedia funcional dos maxilares |
| `dentistica.png` | Dentística |
| `odontopediatria.png` | Odontopediatria |
| `harmonizacao.png` | Harmonização orofacial |

Nome errado = o ícone não aparece e o card volta pro glifo, sem aviso. Copiar
da tabela.

## Formato

- **Quadrado**, 256×256 ou maior. O site desenha em 60×60, então não precisa
  ser grande — precisa ser nítido.
- **PNG com o círculo colorido preenchendo o quadrado inteiro, de borda a
  borda.** O site recorta o arquivo num círculo (`border-radius:50%` +
  `background-size:cover`). Se o ícone vier pequeno no meio de um quadrado
  transparente, sobra um anel sálvia em volta e fica torto.
- Se preferir entregar **SVG**, mande assim mesmo e eu troco a extensão no CSS
  — pesa menos e não borra em tela grande. Aí a regra do círculo continua
  valendo.

## Sobre o estilo do exemplo que você mandou

O modelo de referência usa um círculo colorido diferente por especialidade
(amarelo, verde, vermelho) com o desenho em traço grosso branco por cima.
Funciona e é didático. Duas coisas a pensar antes de fechar a paleta:

1. **Oito cores fortes lado a lado brigam com o verde da marca.** O site inteiro
   é verde-escuro, sálvia e bege. Uma alternativa é manter o traço do desenho
   igual ao do exemplo e usar oito tons dentro da própria família da marca —
   fica didático do mesmo jeito e continua parecendo o consultório dela.
2. **A grade tem 8 cards, o exemplo tem 3.** Com oito círculos berrantes na
   mesma tela o efeito muda bastante em relação ao print.

Não é impedimento — é só o que costuma aparecer depois que os oito estão
prontos. Se quiser as duas versões pra comparar, dá pra montar.

## Onde ficam os originais

Os arquivos de trabalho vão em `Fotos e Imagens/Icones/` (fora do git). Só os
finais, com os nomes acima, ficam aqui — esta pasta **é** versionada, porque é
ela que o site consome.

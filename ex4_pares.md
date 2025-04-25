# Paridade

A definição mais simples e formal sobre números pares e ímpares em minha opinião é:

"Número **par** é todo o **número inteiro** que quando dividido por dois, resulta em um número inteiro, em todos os outros casos o número é **ímpar**."

A partir dessa definição podemos ter algumas informações úteis:

- Essa é uma propriedade exclusiva dos números inteiros. Enquanto 2 é par pois $2 \div 2 = 1$ e 5 é ímpar pois $5 \div 2 = 2.5$, $1/4$ ou $0.5$ não podem ser par ou ímpar pois não pertencem ao conjunto numérico dos inteiros.
- Todo número divisível por 2 forma pares (eis a origem do termo). Para isso, eles se repetem na sequência de números inteiros a cada 2 números: {2, 4, 6, 8, 10...}. Para encontrarmos o enésimo número par podemos usar:  
  $$ x = x \cdot 2 $$
- Todo número inteiro que, ao ser dividido por 2, resulta em números decimais sempre possui um valor a mais que os pares. Por isso são ímpares, e esses números sempre aparecem na ordem ímpar-par na sequência de números inteiros. Os números ímpares são: {1, 3, 5, 7, 9...}. Já os inteiros seguem: {1, 2, 3, 4, 5, 6, 7, 8, 9, 10...}. Podemos calcular o enésimo número ímpar com:  
  $$ x = 2x - 1 $$
- 0 é um número par, pois é um número inteiro que dividido por 2 resulta nele mesmo.

## Teste de Paridade

Existem muitas formas de determinar programaticamente se um número é par. A mais simples usa um operador matemático básico presente na maioria das linguagens, mas pouco usado na escola: o **módulo**.

> A operação de módulo (normalmente expressa como `mod`, `rem`, ou `%`) é usada para encontrar o **resto** da divisão de um número por outro.  
> Por exemplo: `7 % 3 = 1` e `9 % 3 = 0`.

Todo número divisível por outro tem resto zero quando o dividimos. Como 9 é divisível por 3, então:

$$
9 \div 3 = 3, \quad \text{resto } 0
$$

Podemos aplicar isso para saber se um número é par, pois todo número par é divisível por 2. Exemplo:

### Exemplos

$$
8 \div 2 = 4, \quad \text{resto } 0 \Rightarrow 8 \text{ é par}
$$

$$
77 \div 2 = 38, \quad \text{resto } 1 \Rightarrow 77 \text{ é ímpar}
$$

$$
4346 \div 2 = 2173, \quad \text{resto } 0 \Rightarrow 4346 \text{ é par}
$$

No entanto, há uma forma mais eficiente para grandes números: observar **o último dígito**.  
Se ele for divisível por 2, o número inteiro é par. Por exemplo, o último algarismo de 4346 é 6. Como 6 é divisível por 2, então 4346 é par.


## Exercício 
```
Alguns amigos pediram que você desenvolva um algoritmo que determine o resultado de um jogo de "par ou ímpar",
esse programa vai ser usado para calcular o resultado do Campeonato Mundial de Par ou Ímpar,
o programa vai receber qual é o valor da mão jogada pelo jogador que vence caso ímpar e então o valor da mão jogada 

Entrada:
- Valor int da mão do jogador ímpar
- Valor int da mão do jogador par

Saída:
- Mensagem dizendo "PAR" ou "ÍMPAR"
``` 

<!--
```
Escreva um programa que usuário digita um número inteiro qualquer e caso o número seja par imprime o énesimo esse número par na sequência de pares e caso seja ímpar imprime o enésimo número impar com esse número na sequência de ímpares.

Entrada:
- Valor do tipo int representando número

Saída:
- Enésimo número par se par ou enésimo número ímpar se ímpar.
```
-->

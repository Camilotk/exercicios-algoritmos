# Paridade

A definição mais simples e formal sobre números pares e ímpares em minha opinião é:

"Número **par** é todo o **número inteiro** que quando dividido por dois, resulta em um número inteiro, em todos os outros casos o número é **ímpar**."

A partir dessa definição podemos ter algumas informações úteis.

- Essa é uma propriedade exclusiva dos números inteiros, enquanto 2 é par pois \( \frac{2}{2} = 1 \) e 5 é ímpar pois \( \frac{5}{2} = 2.5 \), *\( \frac{1}{4} \) ou 0.5 não podem ser par ou ímpar pois não pertencem ao conjunto numérico dos inteiros*.
- Todo número divisível por 2 forma pares (eis a origem do termo), para isso eles se repetem na sequência de números inteiros a cada 2 números. \{2, 4, 6, 8, 10...\} Para encontrarmos o enésimo número par podemos usar \( x = x \cdot 2 \).
- Assim como todo número inteiro que dividido por 2 resulta em números decimais sempre possui um valor a mais que os pares, por isso são ímpares e esses números sempre aparecem na ordem ímpar-par na sequência de números inteiros, sendo os números ímpares \{1, 3, 5, 7, 9...\}, seguidos. Ou seja, os números inteiros são \{1,2,3,4,5,6,7,8,9,10...\} e seguem a sequência ímpar-par-ímpar-par... infinitamente. Podemos calcular o enésimo número ímpar usando \( x = 2x - 1 \).
- 0 é um número par, pois ele é um número inteiro que dividido por 2 resulta nele mesmo.

## Teste de Paridade

Existem muitas formas de determinar algoritmicamente se um número é par, a forma mais simples é simplesmente usar um operador matemático básico que está incluído na maioria das linguagens, mas que acabamos não vendo tanto na escola: o **módulo**.

> A operação de módulo (normalmente expressa usando `mod` (abreviação de *modulus*), `rem` (abreviação de *remainder*), mas que em Python e outras linguagens é representado pelo uso do operador `%`) é usada para encontrar o **resto** da divisão de um número por outro, por exemplo `7 % 3 = 1` e `9 % 3 = 0`.

Isso porque todo número que é divisível por outro tem resto zero quando dividimos um pelo outro. 9 é divisível por 3 pois quando dividimos 9 por 3 essa divisão tem resto 0. 

Podemos aplicar isso para saber se um número é par porque pela regra dos números pares todo número par é divisível por 2. Logo poderíamos:

### Exemplos em LaTeX:

- \( 8 \Rightarrow 8 \div 2 = 4 \text{ , resto 0 } \Rightarrow 8 \text{ é par} \)

- \( 77 \Rightarrow 77 \div 2 = 38 \text{ , resto 1 } \Rightarrow 77 \text{ é ímpar} \)

- \( 4346 \Rightarrow 4346 \div 2 = 2173 \text{ , resto 0 } \Rightarrow 4346 \text{ é par} \)

Porém, há uma forma mais eficiente de saber se um número é par quando trabalhamos com computações grandes (e que pode ser usada matematicamente para testar de forma eficiente se um número é par), pois os números pares — independentemente do número de algarismos — conservam a lei de divisibilidade por 2 em seu **último algarismo**. Ou seja, para saber se 4346 é par, não precisamos dividir o número inteiro por 2 e ver o resto, basta que façamos isso com seu último algarismo. Nesse caso, 6. Como 6 é divisível por 2, sabemos que 4346 é par.

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

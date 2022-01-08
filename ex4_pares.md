# Paridade

A definição mais simples e formal sobre números pares e ímpares em minha opinião é:

"Número **par** é todo o **número inteiro** que quando dividido por dois, resulta em um número inteiro, em todos os outros casos o número é **ímpar**."

A partir dessa definição podemos ter algumas informações úteis.
- Essa é uma propriedade exclusiva dos números inteiros, enquanto 2 é par pois 2/2 = 1 e e 5 é ímpar pois 5/2 = 2.5, *1/4 ou 0.5 não podem ser par ou ímpar pois não pertencem ao conjunto númerico dos inteiros*.
- Todo número dívisivel por 2 formam pares (eis a origem do termo), para isso eles se repetem na sequência de números inteiros a cada 2 números. {2, 4, 6, 8, 10...} para encontrarmos o enésimo numero par podemos usar x = x * 2
- Assim como todo número inteiro que dividido por 2 resulta em números decimais sempre possui um valor a mais que os pares, por isso ímpar e esses números sempre aparecem na ordem semore ímpar-par na sequềncia de números inteiros sendo os números ímpares {1, 3, 5, 7, 9...} seguidos, ou seja os números inteiros são {1,2,3,4,5,6,7,8,9,10...} e seguem a sequência ímpar-par-ímpar-par... infinitamente. Podemos calcular o enésimo número ímpar usando x = 2x-1.
- 0 é um número par, pois ele é número inteiro que dividido por 2 resulta nele mesmo.

## Teste de Paridade

Existem muitas formas de determinar algoritmicamente se um número é par, a forma mais simples é simplesmente usar um operador matemático básico que está incluído na maioria das linguagens, mas que acabamos não vendo-o tanto na escola: o **módulo**.

> A operação de módulo (normalmente expressa usando mod (abreviação de modulus), rem (abreviação de remainder), mas que em Python e outras linguagens é representado pelo uso do operador %) é usada para encontrar o **resto** da divisão de um número por outro, por exemplo 7 % 3 = 1 e 9 % 3 = 0.

Isso porque todo número que é divisível por outro tem resto zero quando dividimos um pelo outro. 9 é dívisivel por 3 pois quando dividimos 9 por 3 essa divisão tem resto 0. 

Podemos aplicar isso para saber se um número é par porque pela regra dos números pares todo número par é divisível por 2. Logo poderiamos:

<br>
<p align="center">
    <img src="https://render.githubusercontent.com/render/math?math=$8 \Rightarrow 8 \div 2 = 4 \text{ , resto 0 } \Rightarrow \text{ 8 é par }$" width="500">
</p>
<br>
<p align="center">
    <img src="https://render.githubusercontent.com/render/math?math=$77 \Rightarrow 77 \div 2 =  \text{ 38, resto 1 } \Rightarrow \text{ 8 é ímpar }$" width="550">
</p>
<br>
<p align="center">
    <img src="https://render.githubusercontent.com/render/math?math=$4346 \Rightarrow 4346 \div 2 = 2173 \text{ , resto 0 } \Rightarrow \text{ 4346 é par }$" width="650">
</p>

Porém há uma forma mais eficiente de saber se um número é par quando trabalhamos com computações grandes (e que pode ser usado matemáticamente para testar de forma eficiente se um número é par), pois os números pares independente do número algarismos conservam a lei de divisibilidade por 2 em seu último algarismo, ou seja para saber se 4346 é par não precisamos dividir o número inteiro por 2 e ver o resto basta que façamos isso com seu último algarismo, nesse caso 6, como 6 é divísivel por 2 sabemos 4346 é par.

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
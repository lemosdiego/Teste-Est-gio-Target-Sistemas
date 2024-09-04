# Teste de Estágio - Target Sistemas

[Confira aqui](https://teste-est-gio-target-sistemas.vercel.app/)


## 1. Sequência de Fibonacci

Escreva um programa na linguagem de sua escolha que, dado um número informado, calcule a sequência de Fibonacci e retorne uma mensagem indicando se o número informado pertence ou não à sequência.

### function verificarNumeroFibonacci(numero) {
  if (numero < 0) return false;

  let a = 0,
    b = 1;
  while (a < numero) {
    [a, b] = [b, a + b];
  }
  return a === numero;
}

function checarNumeroFibonacci() {
  const input = document.getElementById("numero");
  const numero = parseInt(input.value, 10);
  const resultado = document.getElementById("resultado");

  if (isNaN(numero)) {
    resultado.textContent = "Por favor, insira um número válido.";
    return;
  }

  if (verificarNumeroFibonacci(numero)) {
    resultado.textContent = `${numero} pertence à sequência de Fibonacci.`;
  } else {
    resultado.textContent = `${numero} não pertence à sequência de Fibonacci.`;
  }
}

## 2. Contagem de Letras

Escreva um programa que verifique, em uma string, a existência da letra "a" (seja maiúscula ou minúscula), e informe a quantidade de vezes em que ela ocorre.

 function verificarLetrasA() {
   const texto = document.getElementById("texto").value;
   const resultado2 = document.getElementById("resultado2");

   const countMinusculas = (texto.match(/a/g) || []).length;

   const countMaiusculas = (texto.match(/A/g) || []).length;

   if (countMinusculas > 0 || countMaiusculas > 0) {
    resultado2.textContent =
      `A letra "a" minúscula ocorre ${countMinusculas} vez(es) na string. ` +
      `A letra "A" maiúscula ocorre ${countMaiusculas} vez(es) na string.`;
   } else {
    resultado2.textContent =
      'A letra "a" (maiúscula ou minúscula) não ocorre na string.';
  }
}

## 3 - Observe o trecho de código abaixo:

#### int INDICE = 12, SOMA = 0, K = 1; enquanto K < INDICE faça { K = K + 1; SOMA = SOMA + K; } imprimir(SOMA);

#### Ao final do processamento, qual será o valor da variável SOMA?

### SOMA = 77

## 4 - Descubra a lógica e complete o próximo elemento:

### a - 1, 3, 5, 7, 9
Números Ìmpares de 2 em 2

### b - 2, 4, 8, 16, 32, 64, 128
Cada número é o dobro do anterior.

### c - 0, 1, 4, 9, 16, 25, 36, 49
Sequência de quadrados

#### d - 4, 16, 36, 64, 100
Quadrado de números pares

#### e - 1, 1, 2, 3, 5, 8, 13
Seqência de Fibonacci

#### f - 2,10, 12, 16, 17, 18, 19, 200
Números que começam com a letra D

## 5 - Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em salas diferentes. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada. Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?

#### 1 -Ligo o interruptor 1 por uns 15 minutos para aquecer a lampada

#### 2 - desligo o interruptor 1 e ligo o 2

#### 3- vou até a sala, a lampada que está apagada e quente pertence ao interruptor 1,a lampada que está acesa pertence ao interruptor 2, e a lampada apagada e fria pertence ao interruptor 3

# Exercícios Básicos

Nesta pasta você encontrará exercícios fundamentais de algorítmos e pensamento computacional, incluindo:

- Operações aritméticas
- Manipulação de variáveis
- Entrada e saída de dados
- Lógica básica
- Primeiros programas

## Conteúdo

Lista de Exercícios III - Fundamentos da Linguagem C

1) Faça um programa em C para uma loja de tintas. O programa deverá pedir o tamanho em metros quadrados da área a ser pintada.
Considere que a cobertura da tinta é de 1 litro para cada 3 metros quadrados e que a tinta é vendida em latas de 18 litros, que custam R$ 80,00.
Informe ao usuário a quantidades de latas de tinta a serem compradas e o preço total.

```c
#include <stdio.h>
#include <math.h>

int main()
{
    float area;
    float litros;
    float precoTotal;
    int latas;

    printf("digite o tamanho da area: ");
    scanf("%f", &area);

    litros = area / 3;
    latas = ceil(litros / 18);
    precoTotal = latas * 80;

    printf("\n--- Resultado --- \n");
    printf("Quantidade de latas a comprar: %d\n", latas);
    printf("Preco total: R$ %.2f\n", precoTotal);

    return 0;
}
```

2) Um posto está vendendo combustíveis com a seguinte tabela de descontos:

Álcool:
- até 20 litros desconto de 3% por litro
- acima de 20 litros desconto de 5% por litro

Gasolina:
- até 20 litros desconto de 4% por litro
- acima de 20 litros desconto de 6% por litro.

Escreva um programa C que leia o número de litros vendidos, o tipo de combustível (codificado da seguinte forma: A-álcool, G-gasolina), calcule e imprima o valor a ser pago pelo cliente sabendo-se que o preço do litro da gasolina é R$ 2,50 e o preço do litro do álcool é R$ 1,90.

```c
#include <stdio.h>

int main() {
    float litros, preco, desconto, total;
    char tipo;

    printf("Digite a quantidade de litros: ");
    scanf("%f", &litros);

    printf("Digite o tipo de combustivel (A/G): ");
    scanf(" %c", &tipo);

    if (tipo == 'A' || tipo == 'a') {
        if (litros <= 20)
            desconto = 0.03;
        else
            desconto = 0.05;
        preco = 1.90;
    } else {
        if (litros <= 20)
            desconto = 0.04;
        else
            desconto = 0.06;
        preco = 2.50;
    }

    total = litros * preco * (1 - desconto);

    printf("\nValor total a pagar: R$ %.2f\n", total);

    return 0;
}
```

3) Faça um programa que leia uma quantidade de segundos e converta esse valor para:
- horas;
- minutos;
- segundos.

Exemplo:
Digite a quantidade de segundos: 3675

Horas: 1
Minutos: 1
Segundos: 15

```c
#include <stdio.h>

int main() {
    int total_segundos, horas, minutos, segundos;

    printf("Digite a quantidade de segundos: ");
    scanf("%d", &total_segundos);

    horas = total_segundos / 3600;
    minutos = (total_segundos % 3600) / 60;
    segundos = total_segundos % 60;

    printf("\nHoras: %d\n", horas);
    printf("Minutos: %d\n", minutos);
    printf("Segundos: %d\n", segundos);

    return 0;
}
```

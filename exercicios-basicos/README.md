# Exercícios Básicos

Nesta pasta você encontrará exercícios fundamentais de algorítmos e pensamento computacional, incluindo:

- Operações aritméticas
- Manipulação de variáveis
- Entrada e saída de dados
- Lógica básica
- Primeiros programas

## Conteúdo

### Lista de Exercícios II - Fundamentos da Linguagem C

1) O valor pago por um Hotel da Praia de Iracema para seus porteiros é de R$ 10,25 por hora de trabalho. Faça um programa que pergunte ao usuário quantas horas ele trabalhou e imprima na tela o valor do salário a ser recebido por ele.

```c
#include <stdio.h>
int main()
{
  float horas,salario;
  printf("informe a quantidade de horas trabalhadas?");
  scanf("%f", &horas);

  salario = horas * 10.25;
  printf("seu salario é: R$ %2f", salario);
}
```

2) Sabendo que na Faculdade ABC a média mínima é 7,0 e a tolerância de faltas é 15 % da carga horária do curso, faça um programação em C que peça as informações necessárias e informe a situação do usuário.

```c
#include <stdio.h>

int main()
{
    float media, cargaHoraria, faltas, percentualFaltas;
    printf("Sistema Academico\n");
   
    printf("Informe a média do aluno: ");
    scanf("%f",&media);
   
    printf("Informe a carga horario (numero de aulas): ");
    scanf("%f",&cargaHoraria);
   
    printf("Informe o numero de faltas: ");
    scanf("%f",&faltas);
   
    percentualFaltas = (faltas / cargaHoraria) * 100;
   
    printf ("\n --- RESULTADO --- \n");
    printf ("Media: %.2f\n",media);
    printf ("Percentual de faltas: %.2f\n",percentualFaltas);
   
    if (media >= 7.0 && percentualFaltas <= 15.0)
       printf ("Situação: APROVADO\n");
    else printf ("Situação: REPROVADO\n");
   
    return 0;
}
```

3) Faça um programa que leia dados de um funcionário e calcule seu salário líquido.

**Versão Inicial:**

```c
#include <stdio.h>

int main()
{
    char nome[100];
    char endereco[100];
    char sexo;
    char cidade[50];
    char estado[3];
    int idade;
   
    float salarioBruto;
    float valeTransporte, valeAlimentacao, planoSaude;
    float totalDescontos, salarioLiquido;

    printf(" Cadastro do Funcionário \n");
   
    printf("Nome: ");
    scanf(" %[^\n]", nome);

    printf("Endereço: ");
    scanf(" %[^\n]", endereco);

    printf("Sexo (M/F/Outro): ");
    scanf(" %c", &sexo);

    printf("Cidade: ");
    scanf(" %[^\n]", cidade);

    printf("Estado (UF ex: SP, RJ): ");
    scanf(" %2s", estado);

    printf("Idade: ");
    scanf("%d", &idade);

    printf("Salário Bruto (R$): ");
    scanf("%f", &salarioBruto);

    valeTransporte = salarioBruto * 0.02;  
    valeAlimentacao = salarioBruto * 0.05;
    planoSaude = salarioBruto * 0.10;      

    totalDescontos = valeTransporte + valeAlimentacao + planoSaude;
    salarioLiquido = salarioBruto - totalDescontos;
    printf("        COMPROVANTE DE PAGAMENTO     \n");
    printf("Nome: %s\n", nome);
    printf("Endereço: %s\n", endereco);
    printf("Cidade/UF: %s/%s\n", cidade, estado);
    printf("Sexo: %c | Idade: %d anos\n", sexo, idade);
    printf("-------------------------------------\n");
    printf("Salário Bruto: R$ %.2f\n", salarioBruto);
    printf("-------------------------------------\n");
    printf("Descontos:\n");
    printf("  - Vale Transporte (2%%): R$ %.2f\n", valeTransporte);
    printf("  - Vale Alimentação (5%%): R$ %.2f\n", valeAlimentacao);
    printf("  - Plano de Saúde (10%%):   R$ %.2f\n", planoSaude);
    printf("Total de Descontos:      R$ %.2f\n", totalDescontos);
    printf("-------------------------------------\n");
    printf("SALÁRIO LÍQUIDO:         R$ %.2f\n", salarioLiquido);
    printf("=====================================\n");

    return 0;
}
```

**Versão Corrigida:**

```c
#include <stdio.h>

int main()
{
    char nome[100];
    char endereco[100];
    char sexo;
    char cidade[50];
    char estado[50];
    int idade;
   
    float salarioBruto;
    float valeTransporte, valeAlimentacao, planoSaude;
    float salarioLiquido;

    printf(" Sistema calculo de Salário \n");
    printf("Nome: ");
    scanf(" %[^\n]", nome);
    printf("Endereço: ");
    scanf(" %[^\n]", endereco);
    printf("Sexo ");
    scanf(" %c", &sexo);
    printf("Cidade ");
    scanf(" %[^\n]", cidade);
    printf("Estado ");
    scanf(" %[^\n]", estado);
    printf("Idade ");
    scanf("%d", &idade);
    printf("Salário Bruto (R$): ");
    scanf("%f", &salarioBruto);
   
    valeTransporte = salarioBruto * 0.02;
    valeAlimentacao = salarioBruto * 0.02;
    planoSaude = salarioBruto * 0.02;
    salarioLiquido = salarioBruto - valeTransporte - valeAlimentacao - planoSaude;
    printf("\n Salário liquido \n");
    printf("\n Nome... %s\n",nome);
    printf("\n (-)salarioBruto...: R$ %.2f",salarioBruto);
    printf("\n (-)valeTransporte...: R$ %.2f",valeTransporte);
    printf("\n (-)valeAlimentacao...: R$ %.2f",valeAlimentacao);
    printf("\n (-)planoSaude...: R$ %.2f",planoSaude);
    printf("\n salarioLiquido...: R$ %.2f",salarioLiquido);
    return 0;
}
```

### Lista de Exercícios III - Fundamentos da Linguagem C

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
até 20 litros desconto de 3% por litro
acima de 20 litros desconto de 5% por litro

Gasolina:
até 20 litros desconto de 4% por litro
acima de 20 litros desconto de 6% por litro.

Escreva um programa C que leia o número de litros vendidos, o tipo de combustível (codificado da seguinte forma: A-álcool, G-gasolina), calcule e imprima o valor a ser pago pelo cliente sabendo-se que o preço do litro da gasolina é R$ 6,77 o preço do litro do álcool é R$ 4,34.


```c
#include <stdio.h>

int main() {
    float litros, precoCombustivel, desconto, valorTotal;
    char tipoCombustivel;

    printf("Informe o numero de litros vendidos: ");
    scanf("%f", &litros);
    
    printf("Informe tipo do combustível A - Alcool ou G - Gasolina..: ");
    scanf(" %c", &tipoCombustivel);

    if (tipoCombustivel=='G' || tipoCombustivel=='g'){
        precoCombustivel = 6.77;
        if (litros > 20)
            desconto = 0.06;
        else 
            desconto = 0.04;
    } else if (tipoCombustivel=='A' || tipoCombustivel=='a'){
        precoCombustivel = 4.34;
        if (litros > 20)
            desconto = 0.05;
        else 
            desconto = 0.03;
    } else {
        printf("Tipo de combustível inválido!!!");
        return 1;
    }

    valorTotal = (litros * precoCombustivel) * (1 - desconto);
    printf("Valor a ser pago: R$ %.2f\n", valorTotal);

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

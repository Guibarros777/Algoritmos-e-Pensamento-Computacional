# Exercícios Básicos

Nesta pasta você encontrará exercícios fundamentais de algorítmos e pensamento computacional, incluindo:

- Operações aritméticas
- Manipulação de variáveis
- Entrada e saída de dados
- Lógica básica
- Primeiros programas

## Conteúdo

### CÓDIGOS EM SALA
``` 
CÓDIGOS EM SALA
Declare
       nota1,  nota2, nota3, media
início
      escreva “Informe a nota 1”
      leia nota1
      escreva “Informe nota 2”
      leia nota2
      escreva ”Informe nota3”
      leia nota 3

      media = (nota1 + nota2 + nota3)/3
se ( media>=6) 
      então escreva “Aprovado”
      então escreva “Reprovado”
      escreva “A média é”, media
fim

COMPILADO EM C:
int main() {
    float n1, n2, n3, media;


    printf("Nota 1: ");
    scanf("%f", &n1);


    printf("Nota 2: ");
    scanf("%f", &n2);


    printf("Nota 3: ");
    scanf("%f", &n3);


    media = (n1 + n2 + n3) / 3;
    if(media >= 6) {
        printf("Aprovado\n");
        }else{("Reprovado\n");}
    printf("Media: %.1f\n", media);


    return 0;
}

Calculadora Simples
int main() {
    float num1, num2, resultado;
    char operador;
    
    printf("Digite o primeiro número: ");
    scanf("%f", &num1);
    
    printf("Digite o operador (+, -, *, /): ");
    scanf(" %c", &operador);
    
    printf("Digite o segundo número: ");
    scanf("%f", &num2);
    
    switch(operador) {
        case '+':
            resultado = num1 + num2;
            break;
        case '-':
            resultado = num1 - num2;
            break;
        case '*':
            resultado = num1 * num2;
            break;
        case '/':
            if (num2 != 0) {
                resultado = num1 / num2;
            } else {
                printf("Erro: Divisão por zero!\n");
                return 1;
            }
            break;
        default:
            printf("Operador inválido!\n");
            return 1;
    }
    
    printf("%.2f %c %.2f = %.2f\n", num1, operador, num2, resultado);
    return 0;
}
Conversor de Temperatura

#include <stdio.h>

int main() {
    float temperatura, convertida;
    char escala;
    
    printf("Digite a temperatura: ");
    scanf("%f", &temperatura);
    
    printf("Digite a escala (C para Celsius, F para Fahrenheit): ");
    scanf(" %c", &escala);
    
    if (escala == 'C' || escala == 'c') {
        convertida = (temperatura * 9.0 / 5.0) + 32.0;
        printf("%.2f°C = %.2f°F\n", temperatura, convertida);
    } else if (escala == 'F' || escala == 'f') {
        convertida = (temperatura - 32.0) * 5.0 / 9.0;
        printf("%.2f°F = %.2f°C\n", temperatura, convertida);
    } else {
        printf("Escala inválida!\n");
        return 1;
    }
    
    return 0;
}
—------------------------------------------------------------------------------------------------------------------------
ATIVIDADE 

1:PROGRAMA “QUAL NÚMERO É MAIOR?
#include <stdio.h>
int main() {
    float n1, n2, n3;


    printf("Digite o primeiro número: ");
    scanf("%f", &n1);


    printf("Digite o segundo número: ");
    scanf("%f", &n2);


    printf("Digite o terceiro número: ");
    scanf("%f", &n3);


    if (n1 >= n2 && n1 >= n3) {
        printf("O maior número é: %.2f\n", n1);} 
        else if (n2 >= n1 && n2 >= n3) {
        printf("O maior número é: %.2f\n", n2);} 
        else
        { printf("O maior número é: %.2f\n", n3);} 
    return 0;}


2:EMPRÉSTIMO
#include <stdio.h>
int main() {
    float salario, prestacao;

    printf("Digite o valor do salário: ");
    scanf("%f", &salario);

    printf("Digite o valor da prestação: ");
    scanf("%f", &prestacao);

    if (prestacao > salario * 0.20) {
        printf("Empréstimo não concedido.\n");
    } else {
        printf("Empréstimo concedido.\n");
    }
    return 0;}


3:PESO IDEAL

#include <stdio.h>

int main() {
    float altura, peso_ideal;
    char sexo;

    printf("Digite a altura (em metros, ex: 1.75): ");
    scanf("%f", &altura);

    printf("Digite o sexo (M para Masculino, F para Feminino): ");
    scanf(" %c", &sexo);

    if (sexo == 'M' || sexo == 'm') {
        peso_ideal = (72.7 * altura) - 58;
        printf("O peso ideal para um homem de %.2fm e: %.2f kg\n", altura, peso_ideal);
    } 
    else if (sexo == 'F' || sexo == 'f') {
        peso_ideal = (62.1 * altura) - 44.7;
        printf("O peso ideal para uma mulher de %.2fm e: %.2f kg\n", altura, peso_ideal);
    } 
    else {
        printf("Opcao de sexo invalida! Use apenas 'M' ou 'F'.\n");
    }

    return 0;
}


``` 

### Lista de Exercícios II - Fundamentos da Linguagem C

1) O valor pago por um Hotel da Praia de Iracema para seus porteiros é de R$ 10,25 por hora de trabalho. Faça um programa que pergunte ao usuário quantas horas ele trabalhou e imprima na tela o[...]

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

2) Sabendo que na Faculdade ABC a média mínima é 7,0 e a tolerância de faltas é 15 % da carga horária do curso, faça um programação em C que peça as informações necessárias e informe [...]

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
    scanf(" %[^
", nome);

    printf("Endereço: ");
    scanf(" %[^
", endereco);

    printf("Sexo (M/F/Outro): ");
    scanf(" %c", &sexo);

    printf("Cidade: ");
    scanf(" %[^
", cidade);

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
    scanf(" %[^
", nome);
    printf("Endereço: ");
    scanf(" %[^
", endereco);
    printf("Sexo ");
    scanf(" %c", &sexo);
    printf("Cidade ");
    scanf(" %[^
", cidade);
    printf("Estado ");
    scanf(" %[^
", estado);
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

Escreva um programa C que leia o número de litros vendidos, o tipo de combustível (codificado da seguinte forma: A-álcool, G-gasolina), calcule e imprima o valor a ser pago pelo cliente sabend[...]


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

#include <stdio.h>

int main() {

// Pais 1
char pais [20]= "Reino Unido";
int populacao = 69; //milhões
float area = 243.000; // km²
float pib = 3.84; //trilhões
int turisticos = 23221; // Mil 

// Calculo da Densidade Demografica:  Pais 1
float densidade = populacao / area;


// Pais 2
char pais2 [13]= "Australia";
int populacao2 = 27; //Milhões
float area2 = 7.7; // Milhões km²
float pib2 = 1.75; // Trilhões 
int pontos = 6000; // Mil 

// Calculo da Densidade Demografica:  Pais 2
float densidade2 = populacao2 / area2;

int opcao1, opcao2;
float valor1A , valor2A;
float valor1B , valor2B ;
float somapais1 , somapais2;



//Menu
 printf("Escolha o atributo para comparar as cartas:\n");
 printf("1 - Populacao\n");
 printf("2 - Area\n");
 printf("3 - PIB\n");
 printf("4 - Pontos Turisticos\n");
 printf("5 - Densidade Demografica\n");
 printf("Digite sua opcao: ");
 scanf("%d", &opcao1);

 //Escolha da 2° Carta
    printf("Escolha outro  atributo: \n");
    scanf("%d",&opcao2);




if (opcao1==opcao2){
    printf( "Você escolheu o mesmo atributo duas vezes!\n");
    opcao2=0; // igonara o segundo
}


// Primeiro atributo
char atributo1[30], atributo2[30];


switch (opcao1)
{
case 1: valor1A = populacao; valor2A = populacao2; printf("Populacao (milhoes)\n\n",atributo1); break;
case 2: valor1A = area;  valor2A = area2; printf("Area (km²)\n\n",atributo1); break;
case 3: valor1A = pib;  valor2A = pib2; printf("PIB (trilhoes)\n\n",atributo1); break;
case 4: valor1A = turisticos; valor2A = pontos; printf("Pontos Turísticos (mil)\n\n",atributo1); break;
case 5: valor1A = densidade; valor2A = densidade2; printf("Densidade Demográfica\n\n",atributo1); break;
 default: printf("Opcao invalida!n/"); return  0;

}


// Segunda Opção

switch (opcao2)
{
case 1: valor1B = populacao; valor2B = populacao2; printf("Populacao (milhoes)\n\n",atributo2); break;
case 2: valor1B = area;  valor2B = area2; printf("Area (km²)\n\n",atributo2); break;
case 3: valor1B = pib;  valor2B = pib2; printf("PIB (trilhões)\n\n",atributo2); break;
case 4: valor1B = turisticos; valor2B = pontos; printf("Pontos Turísticos (mil)\n\n",atributo2); break;
case 5: valor1B = densidade; valor2B = densidade2; printf("Densidade Demografica\n\n",atributo2); break;
 default: printf("Opcao invalida!n/"); return  0;

    
}


// Soma total dos atributos
somapais1 = valor1A + valor1B;
somapais2 = valor2A + valor2B;


// Exibição organizada
printf(" RESULTADO DA COMPARAÇÃO \n\n");

printf("Pais: %s\n", pais, pais2);

printf("-------------------------------------\n");
printf("Atributo 1: %s\n", atributo1);
printf("%-15s: %.3f\n", pais, valor1A);
printf("%-15s: %.3f\n", pais2, valor2A);
printf("-------------------------------------\n");
printf("Atributo 2: %s\n", atributo2);
printf("%-15s: %.3f\n", pais, valor1B);
printf("%-15s: %.3f\n", pais2, valor2B);
printf("-------------------------------------\n");
printf("Soma total dos atributos:\n");
printf("%-15s: %.3f\n", pais, somapais1);
printf("%-15s: %.3f\n", pais2, somapais2);

// Exibição final com OPERADOR TERNÁRIO
(somapais1 > somapais2) ? 
    printf(" %s venceu a comparacao geral!\n", pais) :
(somapais2 > somapais1) ? 
    printf(" %s venceu a comparacao geral!\n", pais2) :
    printf(" Houve um empate geral!\n");



return 0;




}

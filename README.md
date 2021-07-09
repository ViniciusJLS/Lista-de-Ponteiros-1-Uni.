# Lista-de-Ponteiros-1-Uni.
Questão 1º)
#include <stdio.h>
#include <stdlib.h>

int main() {
    /*A utilização de ponteiros na engenharia permite que o engenheiro resolva alguns problemas com uma facilidade maior
    tendo em vista que o ponteiro serve para acessar o endereço em que o valor está na memoria, e não o valor em si, esses
    usos para ponteiros é bem visto em arrays, que são um consjunto de valores em sequência e o ponteiro indicia o inicio desse array,= */
return 0;
}

Questão 2º)

#include <stdio.h>
#include <stdlib.h>

int main(){

int i=3,j=5;
int *p, *q;
p = &i;
q = &j;

p == &i;
printf("%d", p);
printf("\n");// resposta = 6422036

*p - *q;
printf("%d", *p - *q);
printf("\n");// resposta = -2

**&p;
printf("%d", **&p);
printf("\n");// resposta = 3

3 - *p/(*q) + 7;
printf("%d", 3 - *p/(*q) + 7);
printf("\n");// resposta = 10

}

Questão 3º)
#include <stdio.h>
#include <stdlib.h>

int main(){
  int i=5, *p;
  &i = 4094;
  p = &i;
  printf("%x %d %d %d %d", p,*p+2,**&p,3**p,**&p+4);
  return 0;
  //p = 61fe1c, *p+2 = 7, **&p = 5, 3**p = 15, **&p+4 = 9
}

Questão 4º)
#include <stdio.h>
#include <stdlib.h>

int main() {
    int i, j;
    int *p, *q;
    p = &i;
    printf("%d", p);
    printf("\n");

    *q = &j;
    printf("%d", q);
    printf("\n");//sem problema

    p = &*&i;
    printf("%d", p);
    printf("\n");//sem problema

    //i = (*&)j;
    printf("%d", i);
    printf("\n");//problema

    i = *&j;
    printf("%d", i);
    printf("\n");//sem porblema

    //i = &&j;
    printf("%d", i);
    printf("\n");//problema

    q = *p;
    printf("%d", q);
    printf("\n");//sem problema

    i = (*p) + *q;
    printf("%d", i);
    printf("\n");//problema
return 0;
}

Questão 5º)
#include <stdio.h>
#include <stdlib.h>

int main() {
  int valor;
  int *p1;
float temp;
  float *p2;
  char aux;
  char *nome = "Ponteiros";
  char *p3;
  int idade;
  int vetor[3];
  int *p4;
  int *p5;

  /* (a) */
  valor = 10;
  p1 = &valor;
  *p1 = 20;
  printf("%d \n", valor);
  //Correto - 20

  /* (b) */
  temp = 26.5;
  p2 = &temp;
  *p2 = 29.0;
  printf("%.1f \n", temp);
  //Correto - 29.0

  /* (c) */
  p3 = &nome[0];
  aux = *p3;
  printf("%c \n", aux);
  //Correto - P

  /* (d) */
  p3 = &nome[4];
  aux = *p3;
  printf("%c \n", aux);
  //Correto - e

  /* (e) */
  p3 = nome;
  printf("%c \n", *p3);
  //Correto - P

  /* (f) */
  p3 = p3 + 4;
  printf("%c \n", *p3);
  //Correto - e

  /* (g) */
  p3--;
  printf("%c \n", *p3);
  //Correto - t

  /* (h) */
  vetor[0] = 31;
  vetor[1] = 45;
  vetor[2] = 27;
  p4 = vetor;
  idade = *p4;
  printf("%d \n", idade);
  //Correto - 31

   /* (i) */
  p5 = p4 + 1;
  idade = *p5;
  printf("%d \n", idade);
  //Correto - 45

  /* (j) */
  p4 = p5 + 1;
  idade = *p4;
  printf("%d \n", idade);
  //Correto - 27

  /* (l) */
  p4 = p4 - 2;
  idade = *p4;
  printf("%d \n", idade);
  //Correto -31

  /* (m) */
  p5 = &vetor[2] - 1;
  printf("%d \n", *p5);
  //Correto - 45

  /* (n) */
  p5;
  printf("%d \n", *p5);
  //Correto - 45
  return(0);
}

Questão 6º)
#include <stdio.h>
#include <stdlib.h>

int main(void){
  float vet[5] = {1.1,2.2,3.3,4.4,5.5};
  float *f;
  int i;
  f = vet;
  printf("contador/valor/valor/endereco/endereco");
  for(i = 0 ; i <= 4 ; i++){
  printf("\ni = %d-",i);
  printf("vet[%d] = %.1f-",i, vet[i]);
  printf("*(f + %d) = %.1f-",i, *(f+i));
  printf("&vet[%d] = %X-",i, &vet[i]);
  printf("(f + %d) = %X",i, f+i);
  //O Contador está correto, O valor 1 indicado está correto, valor 2 está correto , enderenco 1 está correto, enderenco 2 está correta .
    //i = 0-vet[0] = 1.1-*(f + 0) = 1.1-&vet[0] = 61FDF0-(f + 0) = 61FDF0
    //i = 1-vet[1] = 2.2-*(f + 1) = 2.2-&vet[1] = 61FDF4-(f + 1) = 61FDF4
    //i = 2-vet[2] = 3.3-*(f + 2) = 3.3-&vet[2] = 61FDF8-(f + 2) = 61FDF8
    //i = 3-vet[3] = 4.4-*(f + 3) = 4.4-&vet[3] = 61FDFC-(f + 3) = 61FDFC
    //i = 4-vet[4] = 5.5-*(f + 4) = 5.5-&vet[4] = 61FE00-(f + 4) = 61FE00
  }
}

Questão 7º)
#include <stdio.h>
#include <stdlib.h>

int main() {
    int pulo[5] = {1, 2, 3, 4, 5};
    printf("%d", *(pulo + 2));
    printf("\n");
    printf("%d", *(pulo + 4));
    printf("\n");
    printf("%d", (pulo + 4));
    printf("\n");
    printf("%d", (pulo + 2));
    // *(pulo + 2) referencia o valor do terceiro elemento do vetor.
}

Questão 8º)
#include <stdio.h>
#include <stdlib.h>

int main() {
    int mat[4], *p, x;
    p = mat + 1;
    printf("%d", p);// Valida, já que, mostra onde mat está localizado na memoria 4 bytes a frente do mat original.
    //p = mat;`
    printf("\n");
    printf("%d", p);//Invalida, não compilou graças a uma crase.
    //p =`mat;
    printf("\n");
    printf("%d", p);//Invalida, não compilou graças a uma crase.
    x = (*mat);
    printf("\n");
    printf("%d", x);// Valida, já que, está associadp ao valor do conteudo de mat.
    return 0;
}

Questão 9º)
int main(){
  int vet[] = {4,9,13};
  int i;
  for(i=0;i<3;i++){
  printf("%d ",*(vet+i));
  }
}
//O primeiro imprime os valore 4, 9, 13 nessa mesma ordem.

int main(){
  int vet[] = {4,9,13};
  int i;
  for(i=0;i<3;i++){
  printf("%X ",vet+i);
  }
}
//O segundo imprime 61FE10, 61FE14, 61FE18 que são os locais onde os valores 4, 9, 13 se encontram respectivamente.

Questão 10º)
#include <stdio.h>
#include <stdlib.h>

/*Considerando que x esteja armazenado no endereço de memória 4092, supondo também que na máquina
seja usada uma variável do tipo char ocupa 1 byte, do tipo int ocupa 2 bytes, do tipo float ocupa
4 bytes e do tipo double ocupa 8 bytes, os valores de x+1, x+2 e x+3 quando:*/

/*x for declarado como char: Começando pelo endereço de memória 4092 ira saltar para 4093, 4094, 4095*/
/*x for declarado como int: Começando pelo endereço de memória 4092 ira saltar para 4094, 4096, 4098*/
/*x for declarado como float: Começando pelo endereço de memória 4092 ira saltar para 4096, 4100, 4104*/
/*x for declarado como double: Começando pelo endereço de memória 4092 ira saltar para 4100, 4108, 4116*/

int main(){
    char x[4];
    int y[4];
    float z[4];
    double a[4];

    printf("Enderecos para variavel do tipo Character\n ");
    printf("%p\t",x);
    printf("%p\t",x+1);
    printf("%p\t",x+2);
    printf("%p\t",x+3);

    printf("\n");
    printf("\n");

    printf("Enderecos para variavel do tipo Inteiro\n ");
    printf("%p\t",y);
    printf("%p\t",y+1);
    printf("%p\t",y+2);
    printf("%p\t",y+3);

    printf("\n");
    printf("\n");

    printf("Enderecos para variavel do tipo Float\n ");
    printf("%p\t",z);
    printf("%p\t",z+1);
    printf("%p\t",z+2);
    printf("%p\t",z+3);

    printf("\n");
    printf("\n");

    printf("Enderecos para variavel do tipo Double\n ");
    printf("%p\t",a);
    printf("%p\t",a+1);
    printf("%p\t",a+2);
    printf("%p\t",a+3);

    return 0;
}

/*Depois de executar o codigo vemos que a variavel do tipo int ocupa 4 bytes, diferente do que foi feito na suposição(que tinha dado 2 bytes). */
/*O programa satisfez o resto das suposições.*/

Questão 11º)
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int main(){
    float aloha[10], coisas[10][5], *pf, value = 2.2;
    int i=3;

    //  Programa não compila na letras invalidas

    /* a */
    aloha[2] = value;
    printf("%f", aloha[2]);
    //valido

    /* b */
    scanf("%f", &aloha);
    //valido

    /* c */
    aloha = "value";
    //invalido

    /* d */
    printf("%f", aloha);
    //valido

    /* e */
    coisas[4][4] = aloha[3];
    //valido

    /* f */
    coisas[5] = aloha;
    //invalido

    /* g */
    pf = value;
    //invalido
    /* h */
    pf = aloha;
    //valido

}

Questão 12º)
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

/* ponteiros para funções servem para guardar endereços de areas de código,os ponteiros para funções possibilitam a utilizaçãode ponteiros para chamada de funções
o local em que função será executada é feita em um outro ponto do código, fazendo o ponteiro apontar para a função desejada.*/

int potenciacao (int a, int b){
    int resultado;
    resultado = pow(a, b);
    return resultado;
}

int main(){
	int(*p1)(int, int)= potenciacao; //
	int c, a = 4, b = 2;
	c = p1(a, b);
	printf("Valor de a elevado a b = %d", c);
    return 0;
}

Questão 13º)
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int main(){
    float *vetor;
    int x; //Quantidade de numeros que faram parte do vetor.
    int i, aux, j;/*indices utilixades como auxilio para pecorrer o vetor, no caso do i e j(tambem determinaram quais valores serão comparados)
                    a variavel auxiliar serve para fazer essa manipulação dos valores depois da comparação dos dois numeros.*/


    setlocale(LC_ALL, "");
    printf("Informe quantos numeros serão digitados para colocar na ordem cresente: ");
    scanf("%d",&x);
    vetor = (void*)malloc(x * sizeof(int));
    for (i = 0; i < x; ++i) {
         vetor[i] = i;
    }
    printf("\nInforme os numeros do que ficarão em ordem crescente : \n");
    printf("\n");
    for(i = 0; i < x; i++){
            printf("x%d = ", i);
            scanf("%f", &vetor[i]);
    }
    for(i = 0; i < x; i++){
        for(j = i+1; j < x; j++){
            if (vetor[i] > vetor[j]){// comparação que determinara a posição do numero dentro do vetor
                aux = vetor[i];
                vetor[i] = vetor[j];
                vetor[j] = aux;
                }
        }
    }
    printf("\nEsses são os numeros em ordem crescente : \n");
    printf("\n");
    for(i = 0; i < x; i++){
        printf("%f  ",vetor[i]);
    }
    printf("\n");
    free(vetor);
}

Questão 14º)
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int comparacao(const void *a, const void *b){//Ponteiro para uma função que compara dois elementos.
    if ( *(float*)a <  *(float*)b ){
    return -1;// permanece os dois numeros nos mesmos lugares
}
    if ( *(float*)a == *(float*)b ){
    return 0;// permanece os dois numeros nos mesmos lugares
}
    if ( *(float*)a >  *(float*)b ){
    return 1;// os numeros trocam de posição
}
}

int main(){
    float *vetor;// ponteiro do vetor.
    int i;// indice do vetor.
    int x;//quantidade de elementos que estarão presente no vetor.

    setlocale(LC_ALL, "");
    printf("Informe quantos numeros serão digitados para colocar na ordem cresente: ");
    scanf("%d",&x); //quantidade de elementos presente no vetor.
    vetor = (void*)malloc(x * sizeof(int));
    for (i = 0; i < x; ++i) {
         vetor[i] = i;
    }
    printf("\nInforme os numeros do que ficarão em ordem crescente : \n");
    printf("\n");
    for(i = 0; i < x; i++){
            printf("x%d = ", i);
            scanf("%f", &vetor[i]);// esses são os elementos presentes no vetor.
    }
    qsort(vetor, x, sizeof(float), comparacao);/* O qsort serve para ordenar uma sequencia de elementos, ele utiliza um ponteiro aonde estão seus dados, o tamanho de dado,
                                            a quantidade de elementos e uma função que permite comparar um elemento com outro para assim fazer a ordenação*/
    printf("\nEsses são os numeros em ordem crescente : \n");
    printf("\n");
    for(i = 0; i < x; i++){
        printf("%f  ",vetor[i]);// elementos após a ordenação que foi feita pelo qsort.
    }
    free(vetor);//libera vetor
}

Questão 15º)
#include <stdio.h>
#include <math.h>
#include <stdlib.h>

int comparador(const void *a, const void *b) {
   if ( *(float*)a <  *(float*)b ){
    return -1;
}
    if ( *(float*)a == *(float*)b ){
    return 0;
}
    if ( *(float*)a >  *(float*)b ){
    return 1;
}
};

int main () {
   int i, val[] = { 100, 2, 65};

   clock_t Tiques[2];
    Tiques[0] = clock();

   //ordenando o vetor
   qsort(val, 3, sizeof(int), comparador);

   //vetor agora organizado
   printf("Vetor organizado na ordem crescente.\n");
   for( i = 0 ; i < 3; i++ ) {
      printf("%i ", val[i]);
   }
   printf("\n");

   return(0);
}

Questão 16º parte 14)
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <time.h>

int comparacao(const void *a, const void *b){//Ponteiro para uma função que compara dois elementos.
    if ( *(float*)a <  *(float*)b ){
    return -1;// permanece os dois numeros nos mesmos lugares
}
    if ( *(float*)a == *(float*)b ){
    return 0;// permanece os dois numeros nos mesmos lugares
}
    if ( *(float*)a >  *(float*)b ){
    return 1;// os numeros trocam de posição
}
}

int main(){
    float *vetor;// ponteiro do vetor.
    int i;// indice do vetor.
    int x;//quantidade de elementos que estarão presente no vetor.

    clock_t Tiques[2];
    Tiques[0] = clock();

    setlocale(LC_ALL, "");
    printf("Informe quantos numeros serão digitados para colocar na ordem cresente: ");
    scanf("%d",&x); //quantidade de elementos presente no vetor.
    vetor = (void*)malloc(x * sizeof(int));
    for (i = 0; i < x; ++i) {
         vetor[i] = i;
    }
    printf("\nInforme os numeros do que ficarão em ordem crescente : \n");
    printf("\n");
    for(i = 0; i < x; i++){
            printf("x%d = ", i);
            scanf("%f", &vetor[i]);// esses são os elementos presentes no vetor.
    }
    qsort(vetor, x, sizeof(float), comparacao);/* O qsort serve para ordenar uma sequencia de elementos, ele utiliza um ponteiro aonde estão seus dados, o tamanho de dado,
                                            a quantidade de elementos e uma função que permite comparar um elemento com outro para assim fazer a ordenação*/
    printf("\nEsses são os numeros em ordem crescente : \n");
    printf("\n");
    for(i = 0; i < x; i++){
        printf("%f  ",vetor[i]);// elementos após a ordenação que foi feita pelo qsort.
    }
    free(vetor);//libera vetor

    Tiques[1] = clock();
    double temp = (Tiques[1] - Tiques[0]) * 1000.0 / CLOCKS_PER_SEC;
    printf("\nO tempo que foi gasto: %g ms.", temp);
    getchar();
    return 0;
    /* o tempo de execução desse programa mais lento que o do 15 visto que,
    esse possui elementos e quantidade de elementos não declarados.*/
}

Questão 16º parte 15)
#include <stdio.h>
#include <math.h>
#include <stdlib.h>
#include <time.h>

int comparador(const void *a, const void *b) {
   if ( *(float*)a <  *(float*)b ){
    return -1;
}
    if ( *(float*)a == *(float*)b ){
    return 0;
}
    if ( *(float*)a >  *(float*)b ){
    return 1;
}
};

int main () {
   int i, val[] = { 100, 2, 65, 43, 56, 77, 55, 12, 67, 33};

   clock_t Tiques[2];
    Tiques[0] = clock();

   //ordenando o vetor
   qsort(val, 10, sizeof(int), comparador);

   //vetor agora organizado
   printf("Vetor organizado na ordem crescente.\n");
   for( i = 0 ; i < 10; i++ ) {
      printf("%i ", val[i]);
   }
   printf("\n");

   Tiques[1] = clock();
    double temp = (Tiques[1] - Tiques[0]) * 1000.0 / CLOCKS_PER_SEC;
    printf("\nO tempo que foi gasto: %g ms.", temp);
    getchar();
    return 0;
    /* o tempo de execução desse programa foi muito mais rapido que o anterior visto que,
    esse possui elementos e quantidade de elementos ja declarados.*/
}

Questão 17º)
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <locale.h>

int main() {
    int x;// Tamanho do vetor, essa é avariavel que o usuario vai decidir pra determinar o tamanho do vetor
    int *vA, *vB, *vC;// esses são os vetores, sendo o vetor C a soma do vetor A e B.
    int i;// utilizado para pecorrer o vetor

    setlocale(LC_ALL, "");
    printf("Determine qual vai ser o tamanho dos vetores: ");
    scanf("%d", &x);
    vA = (void*)malloc(x * sizeof(int));
    vB = (void*)malloc(x * sizeof(int));
    vC = (void*)malloc(x * sizeof(int));
    for (i = 0; i < x; ++i) {
         vA[i] = i;
    }
    for (i = 0; i < x; ++i) {
         vB[i] = i;
    }
    for (i = 0; i < x; ++i) {
         vC[i] = i;
    }
    printf("\nInforme o valor do inteiro detro do primeiro vetor na posição \n");
    printf("\n");
        for(i = 0; i < x; i++){
            printf("x%d = ", i);
            scanf("%d", &vA[i]);
    }
    printf("\nInforme o valor do inteiro detro do segundo vetor na posição \n");
    printf("\n");
        for(i = 0; i < x; i++){
            printf("x%d = ", i);
            scanf("%d", &vB[i]);
    }
    //soma dos vetores.
    printf("\n");
    for (i = 0; i < x; ++i){
         vC[i] = (vA[i] + vB[i]);
    }
    //Vetor resultado da soma dos dois vetores que o usuario escolheu.
    printf("a Soma dos vetores A e B é igual ao vetor C : ");
    for (i = 0; i < x; ++i){
          printf("%d  ", vC[i]);
    }

    printf("\n");
    free(vC);
    free(vA);
    free(vB);

    return 0;
}

Questão 18º)
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <locale.h>

void Multiplicacao(float **MA, float **MB, float **MC, int m, int n, int p){
int resultado = 0;
for (int i = 0; i < m; i++){
    for (int j = 0; j < p; j++){
        for (int k = 0; k < n; k++){
            resultado = resultado + MA[i][k] * MB[k][j];
        }
        MC[i][j] = resultado;
        resultado = 0;
    }
}

};
int main() {
    int x;// Tamanho do vetor, essa é avariavel que o usuario vai decidir pra determinar o tamanho do vetor
    float **MA, **MB, **MC;// esses são os vetores, sendo o vetor C a soma do vetor A e B.
    int i, j, m, n, p;// utilizado para pecorrer o vetor

    setlocale(LC_ALL, "");
    printf("Determine qual vai ser quantidade de linhas da Matriz A: ");
    scanf("%d", &m);
    printf("Determine qual vai ser a quantidade de colunas da Matriz A e de linhas da B : ");
    scanf("%d", &n);
    printf("Determine qual vai ser a quantidade de colunas da Matriz B: ");
    scanf("%d", &p);

    MA =(float**) malloc(m * sizeof(float*));//alocando bloco auxiliar
    MA[0] = (float*)malloc(m * n * sizeof(float));
    for(i = 1; i < m; i++){
        MA[i] = MA[i-1] + n;//fixa os ponteiros.
    }
    MB = (float**) malloc(n * sizeof(float*));//alocando bloco auxiliar
    MB[0] =(float*) malloc(n * p * sizeof(float));
    for(i = 1; i < n; i++){
        MB[i] = MB[i-1] + p;//fixa os ponteiros.
    }
    MC = (float**) malloc(m * sizeof(float*));//alocando bloco auxiliar
    MC[0] = (float*)malloc(m * p * sizeof(float));
    for(i = 1; i < m; i++){
        MC[i] = MC[i-1] + p;//fixa os ponteiros.
    }

    printf("\nInforme os numeros da matriz A na posição: \n");
    printf("\n");
    for(i = 0; i < m; i++){
        for(j = 0; j < n; j++){
            printf("x[%d][%d] = ", i, j);
            scanf("%f", &MA[i][j]);
        }
        printf("\n");
    }
    printf("\nInforme os numeros da matriz B na posição: \n");

        for(i = 0; i < n; i++){
            for(j = 0; j < p; j++){
                printf("x[%d][%d] = ", i, j);
                scanf("%f", &MB[i][j]);
        }
        printf("\n");
    }

    Multiplicacao (MA, MB, MC, m, n, p);


    printf("\nMatriz A: \n");
        for(i = 0; i < m; i++){
            for(j = 0; j < n; j++){
            printf("%f ", MA[i][j]);
        }
        printf("\n");
    }

     printf("\nMatriz B: \n");
        for(i = 0; i < n; i++){
            for(j = 0; j < p; j++){
            printf("%f ", MB[i][j]);
        }
        printf("\n");
    }
    printf("\nMatriz C: \n");
        for(i = 0; i < n; i++){
            for(j = 0; j < p; j++){
            printf("%f ", MC[i][j]);
        }
        printf("\n");
    }
    free(MA[0]);
    free(MA);
    free(MB[0]);
    free(MB);
    free(MC[0]);
    free(MC);
}
Questão 19º)
Questão 20º)

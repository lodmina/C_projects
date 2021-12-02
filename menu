#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
#include <locale.h>
#include <stdbool.h>
#include <ctype.h>
#define MAX 51
/* Ludmila Maria Pereira da Silva - 192080342 */
int tamanho, aux, array[16], menor;
char string[MAX];

int linha(){
    int q;
    for(q = 1; q <= 60; q++)
        putchar('-');
    putchar('\n');
    return 0;}
int chamaMenu(){
        puts("\t\t\tM E N U    P R I N C I P A L");
        puts("PRESSIONE O NÚMERO CORRESPONDENTE A CADA OPÇÃO ABAIXO ");
        puts("1. Informar a quantidade de números a tratar");
        puts("2. Digitar os números");
        puts("3. Informar o menor número");
        puts("4. Informar o maior número");
        puts("5. Retornar o n-ésimo número da lista");
        puts("6. Calcular a soma dos números");
        puts("7. Calcular o produto dos números");
        puts("8. Multiplicar todos os números por um valor");
        puts("9. Calcular a média aritmética dos números");
        puts("10. Informar quantos números estão acima da média aritmética");
        puts("11. Calcular a média ponderada dos números");
        puts("12. Ordenar os números em ordem crescente");
        puts("13. Ordenar os números em ordem decrescente");
        puts("14. Ler string");
        puts("15. Mostrar string lida e o seu tamanho");
        puts("16. Criptografar a string");
        puts("17. Descriptografar a string");
        puts("18. Terminar a execução");
        return 0;
}
int verifica1e2(bool op1, bool op2){
        while(op1==false){
            printf("Digite primeiro o tamanho do array na opção 1!\n");
            break;}
        while(op2==false){
            printf("Digite primeiro os valores do array na opção 2!\n");
            break;}
    return 0;}
int case_1(int tam){
    puts("Informe o tamanho do array: ");
    scanf("%d", &tam);
    while(tam < 5 || tam > 15 ){
        printf("Digite um tamanho entre 5 e 15.\n");
        scanf("%d", &tam);}
    return tam;
}
int case_2(int tam, int aux, int array[]){
    for(int k=0; k<tamanho; k++){
        puts("Digite o valor a ser inserido: ");
        scanf("%d", &aux);
        array[k]=aux;
        while(aux == 00 || (aux%8 == 0 || aux < -100 || aux > 500)){
            printf("Número inválido. Insira novamente um número.\n");
            scanf("%d", &aux);
            array[k]=aux;}}
    return array;}
int case_3(int array[], int tamanho){
    int menor = array[0];
    for(int k=0; k<tamanho; k++){
        if(menor>array[k]){
            menor = array[k];}}
    return menor;}
int case_4(int array[], int tamanho){
    int maior = array[0];
    for(int k=1; k<tamanho; k++){
        if(array[k]>maior){
            maior = array[k];}}
    return maior;}
int case_5(int pos, int array[pos]){
    puts("Digite a posiçao que deseja procurar: \n");
    scanf("%d", &pos);
    while(pos>=tamanho || pos<0){
        printf("Posição inválida! Digite um valor válido.\n");
        scanf("%d", &pos);}
    if(pos<=(tamanho) && pos>=0){
        printf("Valor na posição %d : %d\n", pos, array[pos]);}
    return array[pos];}
int case_6(int soma,int array[]){
    soma = 0;
    for(int k=0; k<tamanho; k++){
        soma += array[k];}
    /*printf("A soma dos numeros é: %d\n", soma);*/
    return soma;}
int case_7(int produto,int array[]){
    produto = 1;
    for(int k=0; k<tamanho; k++){
        produto *= array[k];}
    /*printf("O produto dos numeros é: %d\n", produto);*/
    return produto;}
int case_8(int aux, int array[], int prodnum){
    puts("Digite o número que irá multiplicar o array: \n");
    scanf("%d", &aux);
    while(aux == 0){
        printf("Informe um valor diferente de zero!\n");
        scanf("%d", &aux);}
    if(aux != 0){
        for(int k=0; k<tamanho; k++){
            prodnum = array[k] *= aux;
            printf("O produto por %d é %d\n", aux, prodnum);}}
    return prodnum;
}
int case_9(){
    int soma = 0;
    for(int k=0; k<tamanho; k++){
        soma += array[k];}
    float media = soma/tamanho;
    printf("Média aritmética: %.2f\n", media);
    return media;
}
int case_10(int soma, int media, int maismedia){
    soma = 0;
    maismedia = 0;
    for(int k=0; k<tamanho; k++){
        soma += array[k];}
    media = soma/tamanho;
    for(int k=0; k<tamanho; k++){
        if(array[k]-media > 0){
            maismedia++;}}
    printf("Quantidade de valores acima da média: %d\n", maismedia);
    return maismedia;}
int case_11(){
    int soma = 0;
    int maismedia = 0;
    int somapesos = 0;
    for(int k=0; k<tamanho; k++){
        printf("Digite o peso do valor na posição %d: \n", k+1);
        scanf("%d", &aux);
        somapesos += aux;
        soma += array[k]*aux;}
    float mediapond = soma/somapesos;
    printf("Média ponderada: %.2f\n", mediapond);
    return mediapond;}
void case_12(int aux, int array[]){
    aux=0;
    for(int k=0; k<tamanho; k++){
        for(int j=k+1; j<tamanho; j++){
            if(array[k]>array[j]){
                aux= array[k];
                array[k]=array[j];
                array[j]=aux;}}}
    for(int k=0; k<tamanho;k++){
        printf("%d\n", array[k]);}
        }
void case_13(int aux, int array[]){
    aux=0;
    for(int k=0; k<tamanho; k++){
        for(int j=k+1; j<tamanho; j++){
            if(array[k]<array[j]){
                aux= array[k];
                array[k]=array[j];
                array[j]=aux;}}}
    for(int k=0; k<tamanho;k++){
        printf("%d\n", array[k]);}}
int case_15(str, string){
    printf("A string %s tem tamanho %d.\n", string, strlen(string));
    return strlen(string);
}
int case_18(){
    exit(4);
    return 0;
}
int cripto(){
/*int MAX = 50;*/
    /*char string[50];*/
    /*scanf("%[^\n]", string);*/
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == B[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = A[k][0];}}}}}

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == C[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                        string[i] = A[k][0];}}}}}

     printf("%s", string);
     return string;}
int descripto(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == A[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = B[k][0];}}}}}
     printf("%s", string);}
int cripto_2(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == B[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = A[k+1][0];}}}}}

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == C[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                        string[i] = A[k+1][0];}}}}}

     printf("%s", string);
     return string;
}
int cripto_3(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 28/*antes era 27*/; j++) {
            if(string[i] == B[j][0]) {
                indice = j+1;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = A[k][1];}}}}}

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 28; j++) {
            if(string[i] == C[j][0]) {
                indice = j+1;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                        string[i] = A[k][1];}}}}}

     printf("%s", string);
     return string;}
int cripto_4(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == B[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = A[k+3][0];}}}}}

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == C[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                        string[i] = A[k+3][0];}}}}}

     printf("%s", string);
     return string;
}
int cripto_5(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 29; j++) {
            if(string[i] == B[j][0]) {
                indice = j+2;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = A[k][2];}}}}}

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 29; j++) {
            if(string[i] == C[j][0]) {
                indice = j+2;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                        string[i] = A[k][2];}}}}}

     printf("%s", string);
     return string;}
int descripto_2(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == A[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = B[k-1][0];}}}}}
     printf("%s", string);
}
int descripto_3(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == A[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = B[k-2][0];}}}}}
     printf("%s", string);
}
int descripto_4(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == A[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = B[k-2][-1];}}}}}
     printf("%s", string);
}
int descripto_5(){
    char A[27][1] = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "!", "@", "#", "$", "%", ";", "&", "*", "(", ")", "-", "+", "<", ">", "/",",", " "};
    char B[27][1] = {"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " "};
    char C[27][1] = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " "};

    int indice;
    int tam = strlen(string);

    for(int i = 0; i < tam; i++) {
        for (int j = 0; j < 27; j++) {
            if(string[i] == A[j][0]) {
                indice = j;
                for(int k = 0; k < 27; k++) {
                    if(indice == k) {
                            string[i] = B[k-3][-1];}}}}}
     printf("%s", string);
}
int main(){
    setlocale(LC_ALL, "Portuguese");
	int opcao, maior, pos, soma, produto, maismedia, somapesos, prodnum, k, num_crip;
	float media, mediapond;
    bool op1 = false;
	bool op2 = false;
    bool str1 = false;
    bool str16 = false;

	while(true){

        linha();
        chamaMenu();
        scanf(" %d", &opcao);
        fflush(stdin);

		switch(opcao){

			case 1:{
			if (opcao==1){
                tamanho = case_1(tamanho);
                if(tamanho > 5 || tamanho < 15){
                    array[tamanho];
                    op1 = true;}
                    break;}}

			case 2:{
                while(op1==false){
                        printf("Digite primeiro o tamanho do array na opção 1!\n");
                        break;}
                if(op1==true){
                    case_2(tamanho, aux, array);
                        op2 = true;}
                        break;}
			case 3:{
                    if(op1==true && op2==true){
                        menor=case_3(array,tamanho);
                        printf("Menor numero do array: %d\n", menor);
                        break;}

                    if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 4:{
				if(op1==true && op2==true){
                    maior=case_4(array, tamanho);
                    printf("Maior numero do array: %d\n", maior);
                    break;}
                    if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}


			case 5:{
                if(op1==true && op2==true){
                    case_5(pos,array[pos]);
                    break;}

                if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 6:{
			    if(op1==true && op2==true){
                    soma=case_6(soma, array);
                    printf("A soma dos numeros é: %d\n", soma);
				break;}

				if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}


			case 7:{
			    if(op1==true && op2==true){
                    produto=case_7(produto, array);
                    printf("O produto dos numeros é: %d\n", produto);
                    break;}

				if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 8:{
			    if(op1==true && op2==true){
                    case_8(aux, array, prodnum);
                        break;}

                if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 9:{
			    if(op1==true && op2==true){
                    case_9(soma, media);
                    break;}

				if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}


			case 10:{
			    if(op1==true && op2==true){
                    case_10(soma, media, maismedia);
                    break;}
                if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 11:{
			    if(op1==true && op2==true){
                    case_11(array);
                    break;}

				if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 12:{
			    if(op1==true && op2==true){
                    case_12(aux, array);
                    break;}
                if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

			case 13:{
			    if(op1==true && op2==true){
                    case_13(aux, array);
                    break;}
                if(op1==false || op2==false){
                        verifica1e2(op1, op2);}
                        break;}

            case 14:{
                puts("Insira a string: ");
                gets(string);
                while (strlen(string)>50){
                    puts("Informe uma string de no máximo 50 caracteres.");
                    gets(string);}
                if(strlen(string)<50){
                    str1=true;}break;}
                    break;

            case 15:{
                if(str1==true){
                    case_15(string, string);
                    break;}
                else if(str1==false){printf("Informe primeiro a string na opção 14!\n");}
                break;}


            case 16:{
                if(str1==true){
                    puts("Informe um número entre 1 e 5.");
                    scanf("%d",&num_crip);
                    if (num_crip == 1){
                        cripto(string);
                        str16=true;
                        break;}
                    if(num_crip == 2){
                        cripto_2(string);
                        str16=true;
                        break;}
                    if(num_crip == 3){
                        cripto_3(string);
                        str16=true;
                        break;}
                    if(num_crip == 4){
                        cripto_4(string);
                        str16=true;
                        break;}
                    if(num_crip == 5){
                        cripto_5(string);
                        str16=true;
                        break;}
                    }
                else if(str1==false){printf("Informe primeiro a string na opção 14!\n");}}

            case 17:{
                if(str16==true){
                    if (num_crip==1){
                        descripto(string);
                        break;}
                    if(num_crip==2){
                        descripto_2(string);
                        break;}
                    if(num_crip==3){
                        descripto_3(string);
                        break;}
                    if(num_crip==4){
                        descripto_4(string);
                        break;}
                    if(num_crip==5){
                        descripto_5(string);
                        break;}
                else if(str16==false){printf("Primeiro criptografe a string na opção 16!\n");}}}

			case 18:{
				case_18();
				break;}
			default:
				printf("Escolha uma opção entre 1 e 18.\n");}}

	return 0;
}

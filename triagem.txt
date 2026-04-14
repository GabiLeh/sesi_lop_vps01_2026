#include <stdio.h>
#include <windows.h>
void main(){
	SetConsoleOutputCP(CP_UTF8);
	char pedido, tipo;
	int senha = 0;
	do{
		printf("Possui pedido de exame?(s/n):    ");
		scanf("%c", &pedido);
		if(pedido == 's'){
			senha++;
			printf("Sua senha é %d, ");
			printf("qual o tipo de exame? \n");
			printf("a = admissional \n");
			printf("d = demissional \n");
			printf("p = periódico \n");
			printf("o = outro \n");
			scanf(" %c", &tipo);
			if (tipo == 'a') printf("Encaminhe-se para a sala 1\n");
			else if(tipo == 'd') printf("Encaminhe-se para a sala 2\n");
			else if(tipo == 'p') printf("Encaminhe-se para a sala 3\n");
			else if(tipo == 'o') printf("Encaminhe-se para a sala 4\n");
		}
	}while (pedido == 's');
	printf("Volte para a sua empresa.");
}
# exercicios-em-linguagem-c
lista 1
/*QUESTÃO 02:
Elabore um algoritmo que, dada a idade de um
nadador, classifique-o em uma das seguintes
categorias:
Elabore um algoritmo que, dada a idade de um
nadador, classifique-o em uma das seguintes
categorias:

Categoria Faixa de idade
infantil A 0 - 4 anos
infantil B 5 - 7 anos
infantil C 8-10 anos
juvenil A 11-13 anos
juvenil B 14-17 anos
Adulto 18 anos ou mais

#include <stdio.h>

int main (void)
{
	int idade_i;
	
	printf("Informe a idade: \n");
	scanf("%d", &idade_i);
	
	switch(idade_i)
	{
		case 0:
		case 1:
		case 2:
		case 3:
		case 4:
			
			printf("Infantil A \n");
			break;
			
		case 5:
		case 6:
		case 7:
			printf("Infantil B \n");
			break;
			
		case 8:
		case 9:
		case 10:
			printf("Infantil C \n");
			break;
			
		case 11:
		case 12:
		case 13:
		
			printf("Juvenil A \n");
			break;
		
		case 14:
		case 15:
		case 16:
		case 17:
			printf("Juvenil B \n");
			break;
		default:
			printf("Adulto");
			break;
			
	}
}

-----------------------------------------------------------------------------------------------------------------
/*QUESTÃO 02:


SEGUNDA FORMA
Elabore um algoritmo que, dada a idade de um
nadador, classifique-o em uma das seguintes
categorias:

Categoria Faixa de idade
infantil A 0 - 4 anos
infantil B 5 - 7 anos
infantil C 8-10 anos
juvenil A 11-13 anos
juvenil B 14-17 anos
Adulto 18 anos ou mais

#include <stdio.h>

int main(void)
{
	int idade_i;
	printf("Digite sua idade:");
	scanf("%d", &idade_i);
	
	if(idade_i <=4)
	{
		printf("Infantil A \n");
	}
	
	else
	if(idade_i <=7)
	{
		printf("Infantil B \n");
	}
	
	else
	
	{
		if(idade_i <=10)
			{
				printf("Infantil C \n");
			}
			
			else
			{
				if(idade_i <=13)
				{
					printf("Juvenil A \n");
				}
				else
				{
					if(idade_i <=17)
					{
						printf("Juvenil B \n");	
					}
					else
					{
				
						printf("Adulto \n");
					}
				}
			}
	}
	
	
	
}

-------------------------------------------------------------------------------------------------------------------

/*QUESTÃO 03:
Construir um algoritmo que calcule o peso ideal
de uma pessoa, de acordo com o seu gênero e
altura, utilizando as seguintes fórmulas:
? para homens: (72.7*h)-58
? para mulheres: (62.1*h)-44.7

#include <stdio.h>
# include <ctype.h>
int main (void)
{
	char sexo_c;
	float altura_f, pIdeal_f;
	
	printf("Qual e seu sexo?\n");
	fflush (stdin);	
	scanf("%c", &sexo_c);
	sexo_c =tolower(sexo_c);
	
	printf("Qual e sua altura?\n");
	scanf("%f", &altura_f);
	
	if ((sexo_c == 'f') || (sexo_c == 'm'))
	{
		if(sexo_c == 'f')
		{
			pIdeal_f = (62.1 * altura_f) - 44.7;
		}
		else
		{
			pIdeal_f = (72.7 * altura_f) - 58;
		}
	}
	else
	{
		printf("Valor informado incorreto");
	}
	printf("Seu peso ideal e:%f", pIdeal_f);
	
	return 0;
}


--------------------------------------------------------------------------------------------------------------------------

/* QUESTÃO 04:
Um banco concederá um crédito especial aos
seus clientes, variável com o saldo médio no
último ano. Faça um algoritmo que calcule o
valor do crédito de acordo com a tabela abaixo.
#include <stdio.h>

int main(void)
{
	int saldo_i, credito_i;
	
	printf("Digite seu saldo:");
	scanf("%d", &saldo_i);
	
	if (saldo_i <=999.00)
	credito_i = 0;
	
	else if ((saldo_i >=1000.00) && (saldo_i <=1499.99))
	credito_i = 0.2 * saldo_i;
	
	else if ((saldo_i >=1500.00) && (saldo_i <=2499.99))
	credito_i = 0.3 * saldo_i;
	
	else
	credito_i = 0.4 * saldo_i;
	
	printf("Seu credito eh: R$%d", credito_i);
}

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
int main() {
 FILE *txt;
 char texto[1000];
  char letra;
  int p = 0;
  int n = 0;
 txt = fopen("archivo.txt", "r");
 

 		if (txt != NULL) {
 			printf("El archivo se abrio correctamente.\n");
			 
			 
 			printf("\nContenido del archivo:\n");
 				while(feof(txt) == 0) {
 					fgets(texto, 1000, txt);
 						printf("%s", texto);
 					}
			
		while(!feof(txt)){
			letra=fgetc(txt);
				if(letra==' ')p++;
					if(isdigit(letra))n++;
						fclose(txt);
		txt = fopen("resultado1.txt", "w");
			fprintf(txt ,"Son %d palabras", p);
					fclose(txt);
		txt = fopen("resultado2.txt", "w");
			fprintf(txt ,"Son %d numeros", n);
					fclose(txt);
				}

		} 
		
return 0;	
 }

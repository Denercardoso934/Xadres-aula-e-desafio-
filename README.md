# Xadres-aula-e-desafio-
desafio de xadres em linguagem C 

#include <stdio.h>
#include <string.h>

int main() {
    char peca[20];
    int x1, y1, x2, y2;

    printf("Digite a peca (torre, bispo, cavalo): ");
    scanf("%s", peca);

    printf("Digite a posicao atual (linha e coluna): ");
    scanf("%d %d", &x1, &y1);

    printf("Digite a nova posicao (linha e coluna): ");
    scanf("%d %d", &x2, &y2);

    if (strcmp(peca, "torre") == 0) {
        if (x1 == x2 || y1 == y2) {
            printf("Movimento valido para a torre.\n");
        } else {
            printf("Movimento invalido para a torre.\n");
        }
    } else if (strcmp(peca, "bispo") == 0) {
        if (x1 - x2 == y1 - y2) {
            printf("Movimento valido para o bispo.\n");
        } else {
            printf("Movimento invalido para o bispo.\n");
        }
    } else if (strcmp(peca, "cavalo") == 0) {
        if ((abs(x1 - x2) == 2 && abs(y1 - y2) == 1) || 
            (abs(x1 - x2) == 1 && abs(y1 - y2) == 2)) {
            printf("Movimento valido para o cavalo.\n");
        } else {
            printf("Movimento invalido para o cavalo.\n");
        }

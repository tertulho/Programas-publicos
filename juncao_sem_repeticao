#include <stdio.h>
#include <stdlib.h>

int verificacao_b(int origem , int *final)
{
// verifica se existe alguma peca repetida na colecao. Usado para reconhecer o tamanho exato ta lista final
    int tamanho_r=0;
    int inter = 0;

    for(int z=0; z < origem; z++)
    {
        for (int n=z+1; n<origem ; n++)
        {
            if ( final[z]== final[n])
                inter++;
        }
        if ( inter== 0)
            tamanho_r++;
        inter = 0;
    }
    return tamanho_r;
}


int verificacao(int contador,int origem , int *final){
    // verifica se o item ja foi adicionado anteriormente
    for(int z=0; z < contador; z++)
    {
        if ( final[z]== origem)
        return 0;
    }
    return 1;
}



int* unir_colecoes(int *colecao_herois_hq ,int *colecao_acao_comics,int tamanho_herois_hq,int tamanho_acao_comics , int *tamanho_final)
{
    //Responsavel por organizar os procedimentos
    int cont = 0;
    *tamanho_final = verificacao_b(tamanho_herois_hq,colecao_herois_hq) + verificacao_b(tamanho_acao_comics, colecao_acao_comics);
    
    int *colecao_unificada;

    colecao_unificada = (int *)malloc ( *tamanho_final * sizeof(int) );

    // A adição de cada lista é feita separadamente com a verificacao 
    for(int i = 0; i < tamanho_herois_hq ; i++)
    {
        if (verificacao( cont , colecao_herois_hq[i] , colecao_unificada))
            {
            colecao_unificada[cont] = colecao_herois_hq[i];
            cont++ ;
            }    
    }
    for (int x = 0; x< tamanho_acao_comics; x++)
    {
        if (verificacao(cont , colecao_acao_comics[x], colecao_unificada))
            {
            colecao_unificada[cont] = colecao_acao_comics[x];
            cont++ ;

            }
    }
    
    return colecao_unificada;
} 


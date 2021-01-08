# Cronometro
Cronometro

include <stdio.h>
include <stdlib.h>
include <windows.h>//para usar o sleep
include <MMSystem.h>//para o soom


int main()
{
    int segundo = 55, minuto = 14, hora = 0, i = 0;// s = segundos. m = minutos , h = hora

    system("PAUSE");

    while(i<10){
        system("cls");//limpar a tela
        printf("\n\t %dh: %dm: %ds",hora , minuto,segundo);
        Sleep(935);//tem a função de pausar a tela por um determinado tempo
        segundo++;
        if(segundo == 60){
            segundo = 0;
            minuto++;
        }

        if (minuto == 15){
            minuto = 0;
            segundo = 0;
            PlaySound(TEXT("Elixir.WAV"), NULL, SND_SYNC);
        }
    }


    return 0;
}

//This is rock paper scissor game my first project in my life
//A multiplayer game rock paper scissor 
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#include<math.h>
int rockpaper(char player,char computer)
{
    if(player==computer)
        return -1;
    else if((player=='s' && computer=='z')||(player=='z' && computer=='p')||(player=='p' && computer=='s')){
        return 1;
      }
    else
    return 0;
}
int main()
{
    printf("                    Welcome to the rock paper scissor game                  \n");
    int n,result;
    char ch='y';
    char player,comp;
    while(ch=='y'||ch=='Y'){
        srand(time(NULL));
        n=rand()%100;
            if(n>=0 && n<33){
                comp='s';//stone
            }
        else if(n>=33 && n<66){
                comp='p';//paper
            }
        else{
                comp='z';//scissor
            }
    printf("                  Enter s for-STONE p for-PAPER z for-SCISSOR:");
    scanf(" %c",&player);
    result=rockpaper(player,comp);
    if(result==1){
            printf("\n\t\t\tYou have won the game");
        }
    else if(result==0){
                printf("\n\t\t\tYou have lose the game");
        }
    else{
                 printf("\n\t\t\tIt's a draw game");
        }
    printf("\n");
    printf("\t\t\tYou chose:%c  computer chose:%c\n",player,comp);
    printf("                        Want to play one more game(y/n):");
    scanf(" %c",&ch);
}
    return 0;
}


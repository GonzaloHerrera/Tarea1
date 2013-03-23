#include <cstdlib>
#include <iostream>

using namespace std;


void llenarM(int M[][8])
{
     int cont=1;
     for(int i=0;i<=7;i++)
         for(int j=0;j<=7;j++)
             M[i][j]=0;
     M[7][0]=cont;
     int filas=7;
     int columnas=0;
     
     while(cont!=5)
     {
          cont++;
          int numero=1;
           
          switch(numero)
          {
              case 1:
                   filas=filas-1;
                   columnas=columnas+2;
                   if(filas<0 || filas>7 || columnas <0 || columnas>7)
                   {
                              filas=filas+1;
                              columnas=columnas-2;
                   }
                   else
                   {
                   }
                   M[filas][columnas]=cont;
                   break;
              
          }
                                    
     }
      for(int i=0;i<=7;i++)
          {
             for(int j=0;j<=7;j++)
                 cout<<M[i][j]<<" ";   
             cout<<endl; 
          }          

}


int main(int argc, char *argv[])
{
    int A[8][8];
    llenarM(A);
    
    system("PAUSE");
    return EXIT_SUCCESS;
}
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

    int main(){
    int a , b ,c ;
    float x ;
        do{
            scanf("%d %d %d",&a,&b ,&c );
        } while ( abs(a) > 1000 || abs(b) > 1000 || abs(c) > 1000 );
        if ( a == 0){
            if ( b == 0){
                if ( c == 0 ){
                    printf("WOW");
                }else printf("NO");
            } else  {
                x = -c/b;
                printf ("%.2f",x);
            }
        }
        if (a != 0){
            float delta = b*b - 4*a*c;
            float x1 , x2;
            if (delta < 0 ){
                printf("NO");
            }else if (delta == 0 ){
                float x1 = -b/(2*a);
                float x2 = -b/(2*a);
                printf("%.2f %.2f",x1 , x2 );
            }
            else {
                float    x1 = (-b-sqrt(delta))/(2*a);
            float    x2 = (-b+sqrt(delta))/(2*a);
                printf("%.2f %.2f", x1 , x2 );
            }
        }
        return 0;
}

# UnionExampleforKodegod

Had trouble compiling an example program for the video course c programming theory part dealing with unions so here is the program I got to work with help from more experienced programmers.

additional info on why my first attempts did not work please go to:
https://stackoverflow.com/questions/64706527/when-assigning-a-string-to-a-union-member-defined-as-char-name20-it-will-not-c

#include <stdio.h>
#include <string.h>

union myFirstUnion {
    int i;
    float f;
    char name[20];
} unionVar;   

/* of if }; left blank it can be declared as such: 
union myFirstUnion unionVar; 
*/


int main() {
    unionVar.i = 10;
    printf("%d ", unionVar.i);
    printf("\n");
    strcpy(unionVar.name, "Bill can code");
    printf("%s ", unionVar.name);
    printf("\n");
    unionVar.f = 10.0;
    printf("%f ", unionVar.f);
    printf("\n");
    strcpy(unionVar.name, "June can compute");
    printf("%s ", unionVar.name);
    printf("\n");
    return 0;
}

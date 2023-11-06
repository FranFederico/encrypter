#include <stdio.h>
#include <stdlib.h>
#include <conio.h>


int main()
{
    char fname[50], ch;
    FILE *fps, *fpt;

    printf("Enter Filename: ");       // the file should be in the same directory of this C program
    gets(fname);

    fps = fopen(fname, "r");

    if(fps == NULL)
        return 0;

    fpt = fopen("temp.txt", "w");

    if(fpt == NULL)
        return 0;
    ch = fgetc(fps);

    while(ch != EOF)
    {
        ch = ch+90;
        fputc(ch, fpt);
        ch = fgetc(fps);
    }

    fclose(fps);
    fclose(fpt);
    fps = fopen(fname, "w");

    if(fps == NULL)
        return 0;

    fpt = fopen("temp.txt", "r");

    if(fpt == NULL)
        return 0;
    ch = fgetc(fpt);

    while(ch != EOF)
    {
        ch = fputc(ch, fps);
        ch = fgetc(fpt);
    }

    fclose(fps);
    fclose(fpt);

    printf("\nFile %s Encrypted Successfully!\n", fname);

    return 0;
}


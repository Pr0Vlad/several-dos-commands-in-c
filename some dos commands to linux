#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>

int main() {
    bool x = true;
    char input[100], arg[2][10];
    for(int i = 0; i<9; i++){
        strcpy((char *) arg[i], " ");
        }
    char command[100];
    while(x == true) {
        strcpy((char *) arg[1], " ");
        printf("Enter A Command or type Ctrl-C to quit\n");
        scanf(" %[^\n]%*c", input);
        if (strcmp((const char *) input, "Ctrl-C") == 0) {
            printf("GoodBye");
            break;
        } else {
            char * cmd = strtok((char *) input, " ");
            int i = 0;
            while (cmd != NULL) {
                //   printf("%s\n", cmd );  //for test
                strcpy((char *) arg[i], cmd);
                cmd = strtok(NULL, " ");
                i++;
            }
            if (strcmp((const char *) arg[0], "dir") == 0) {
                system("ls");
            }
        //also need one argument
            else if (strcmp((const char *) arg[0], "cd") == 0) {
                strcpy(command, "");
                if(strcmp((const char *) arg[1], " ") != 0){
                    strcat(command, (const char *) arg[1]);
                }
                chdir(command);
                printf( "%d", system("ls"));
            }
                //also need one argument
            else if (strcmp((const char *) arg[0], "type") == 0) {
                strcpy(command, "cat ");
                if(strcmp((const char *) arg[1], " ") != 0 ) {
                    strcat(command, (const char *) arg[1]);
                    system(command);
                } else
                    printf("No argument try Again:\n ");
            }
                //also need one argument
            else if (strcmp((const char *) arg[0], "del") == 0) {
                strcpy(command, "rm ");
                strcat(command, (const char *) arg[1]);
                system(command);
            }
                //also need two argument
            else if (strcmp((const char *) arg[0], "ren") == 0) {
                strcpy(command, "mv ");
                strcat(command, (const char *) arg[1]);
                strcat(command, " ");
                strcat(command, (const char *) arg[2]);
                system(command);
            }
                //also need two argument
            else if (strcmp((const char *) arg[0], "copy") == 0) {
                strcpy(command, "cp ");
                strcat(command, (const char *) arg[1]);
                strcat(command, " ");
                strcat(command, (const char *) arg[2]);
                system(command);
            }
            else{
                printf("error try again or exit\n");
            }
        }
    }
    return 0;
}

IMPLEMENTATION OF OPENDIR AND READDIR SYSTEM
CALLS
AIM:
To write a program for implementing Directory management using the following system calls of UNIX operating system: opendir, readdir.
ALGORITHM:
1.	Start the program.
2.	Open the directory at specified in command line input.
3.	Display the directory contents.
4.	Stop the program. PROGRAM: #include<sys/types.h> #include<dirent.h> #include<stdio.h> main(int c, char* arg[])
{
DIR *d;
struct dirent *r; int i=0; d=opendir(arg[1]);
printf("\n\t NAME OF ITEM \n"); while((r=readdir(d)) != NULL)
{
printf("\t %s \n",r->d_name); i=i+1;
}
printf("\n TOTAL NUMBER OF ITEM IN THAT DIRECTORY IS %d \n",i);
}
OUTPUT:
[root@localhost ~]# cc dr.c [root@localhost ~]# ./a.out lab_print
NAME OF ITEM pri_output.doc sjf_output.doc fcfs_output.doc rr_output.doc ipc_pipe_output.doc
 
pro_con_prob_output.doc
TOTAL NUMBER OF ITEM IN THAT DIRECTORY IS 8
RESULT:
Thus the program for directory management was written and successfully executed.

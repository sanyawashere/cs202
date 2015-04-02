#include<stdio.h>
#include<stdlib.h>
typedef struct{
	char *name;
	double height;

}student;

void readStudents(char *fileName, student *stds, int size);
void printData(student *std, int size);
int findMin(student *std, int size);

int main(int argc, char *argv[]) //argv is a string
{
	int size = atoi(argv[2]); //defines how many people you want
	int minIndex;
	student stds[20];
	readStudents(argv[1], stds, size); //argv[0] is ./files so ignore
	printData(stds,size);
	findMin(stds,size);
	printf("The Student with min height is: %s\n", stds[minIndex].name);
}
void printData(student *std, int size){
	printf("The Students are: \n");
	for(int i=0; i < size; i++)
	{
		printf("Name: %s - Height:%lf\n",std[i].name, std[i].height);
	
	}
}
void readStudents(char *fileName, student *stds, int size){
	FILE *fp; //file pointer
	fp = fopen(fileName,"r"); // "r" means read mode

	for(int i=0; i < size; i++){
		stds[i].name = new char[30];		
		fscanf(fp, "%s %lf", stds[i].name, &(stds[i].height)); //scans from the file

	}
	fclose(fp); //closes the file
}

int findMin(student *std, int size)
{
	int minIndex = 0;
	for(int i=0; i <size; i++)
	{
		if(std[i].height < std[minIndex].height)
		{
			minIndex = i;
		}
	}
	return minIndex;
			


}

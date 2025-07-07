
#include <stdio.h>
int main()
{
char matrix[3][3];
int i, j;
for (i = 0; i < 3; i++)
{
for (j = 0; j < 3; j++)
{
matrix[i][j] = ' ';
}
}

while (1)
{
int row, col;
char ch;
printf("\nCurrent Matrix:\n");
for (i = 0; i < 3; i++)
{
for (j = 0; j < 3; j++)
{
if (matrix[i][j] == ' ')
printf("null\t");
else
printf("%c\t", matrix[i][j]);
}
printf("\n");
}
printf("\nEnter the Position : ");
scanf("%d %d", &row, &col);
if (matrix[row][col] != ' ')
{
printf(" This position is already filled with '%c'\n", matrix[row][col]);
continue;
}
while (getchar() != '\n');
printf("Enter your string: ");
scanf("%c", &ch);
if (ch != 'x' && ch != 'o')
{
printf("\n ....Game only accept 'x' & 'o' Charecter....");
continue;
}
matrix[row][col] = ch;
}
return 0;
}


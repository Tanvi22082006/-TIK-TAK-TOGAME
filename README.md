
#include <stdio.h><BR>
int main()

char matrix[3][3];<BR>
int i, j;<BR>
for (i = 0; i < 3; i++)<BR>
{<BR>
for (j = 0; j < 3; j++)<BR>
{<BR>
matrix[i][j] = ' ';<BR>
}<BR>
}<BR>

while (1)<BR>
{<BR>
int row, col;<BR>
char ch;<BR>
printf("\nCurrent Matrix:\n");<BR>
for (i = 0; i < 3; i++)<BR>
{<BR>
for (j = 0; j < 3; j++)<BR>
{<BR>
if (matrix[i][j] == ' ')<BR>
printf("null\t");<BR>
else<BR>
printf("%c\t", matrix[i][j]);<BR>
}<BR>
printf("\n");<BR>
}<BR>
printf("\nEnter the Position : ");<BR>
scanf("%d %d", &row, &col);<BR>
if (matrix[row][col] != ' ')<BR>
{<BR>
printf(" This position is already filled with '%c'\n", matrix[row][col]);<BR>
continue;<BR>
}<BR>
while (getchar() != '\n');<BR>
printf("Enter your string: ");<BR>
scanf("%c", &ch);<BR>
if (ch != 'x' && ch != 'o')<BR>
{<BR>
printf("\n ....Game only accept 'x' & 'o' Charecter....");<BR>
continue;<BR>
}<BR>
matrix[row][col] = ch;<BR>
}<BR>
return 0;<BR>
}<BR>


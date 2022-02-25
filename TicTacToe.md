#include <stdio.h> //standar input and output library 
char box[10] = { '0', '1', '2', '3', '4', '5', '6', '7', '8', '9' }; //numbering boxes for board

void creating_board();
void marking_board(int, char);


int main()
{
	char mark; // defining varaible mark 
	int player = 1, choice; //defining intilized varaibles player and choice for our marking baord function 
	
		creating_board(); //call the creating_board function to run 
		player = (player % 2) ? 1 : 2; //define players 1 and 2
		scanf_s(" %d", &choice); //scan for users choice 
		mark = (player == 1) ? 'X' : 'o'; //mark board based on scanned choice 

		marking_board(choice, mark); //call the marking_board function to run in console. 


}

void creating_board() // main function eventually will be named someothing else like "creating_board"
{
	printf("\n\n\tTic Tac Toe\n\n"); //print header 
	printf("Player 1 (x) -- Player 2 (0)\n\n"); // declare players 
	printf("      |     |    \n"); //creating board lines
	printf("  %c   |  %c  |  %c   \n", box[1], box[2], box[3]); //creating the number characters 1, 2, 3
	printf("______|_____|____\n"); //creating board lines
	printf("      |     |    \n"); //creating board lines
	printf("  %c   |  %c  |  %c   \n", box[4], box[5], box[6]); //creating the number characters 4, 5, 6
	printf("______|_____|____\n"); //creating board lines
	printf("      |     |    \n"); //creating board lines
	printf("  %c   |  %c  |  %c   \n", box[7], box[8], box[9]); //creating the number characters 7, 8, 9
	printf("______|_____|____\n"); //creating board lines
	printf("      |     |    \n"); //creating board lines
}


void marking_board(int choice, char mark) //Function for marking the board so players can pick a box number as their selection and after selcetion the fucntion will mark it out with an "X"
{
	//choosing box 1 through 9 will mark an "x"
	if (choice == 1 && box[1] == '1') 
		box[1] = mark;
	else if (choice == 2 && box[2] == '2')
		box[2] = mark;
	else if (choice == 3 && box[3] == '3')
		box[3] = mark;
	else if (choice == 4 && box[4] == '4')
		box[4] = mark;
	else if (choice == 5 && box[5] == '5')
		box[5] = mark;
	else if (choice == 6 && box[6] == '6')
		box[6] = mark;
	else if (choice == 7 && box[7] == '7')
		box[7] = mark;
	else if (choice == 8 && box[8] == '8')
		box[8] = mark;
	else if (choice == 9 && box[9] == '9 ')
		box[9] = mark;
	else
	{
		printf("invalid move"); //if player does not choose a number 1 through 9 then function will print "invalid move"
	}
}

# morsecode
// © copyright 2017  MARIANGEL MORA. All Rights Reserved.
// Author: Mariangel Mora Casanova
// Date: 09-11-2017
// Contact: mariangelmorac@gmail.com
// Description: short description
#include <iostream>
#include <windows.h> // access Sleep(), Beep(), SetConsoleTitle() … library functions
//#include <cstring> // string type access.
#include <string> // library that supports string


using namespace std;
// function prototype

void morseCode(char);
void dot()
{

	Beep(400, 100); // sound of a DOT
	cout << '.'; // print a DOT
	Sleep(1000); // wait for 1ooo milliseconds
}
void dash()
{
	Beep(500, 200); // sound of a DASH
	cout << '-'; // print a DASH
	Sleep(1000); // wait 1ooo milliseconds
}
int main()
{
	string in; // from string
	cout << "Enter a word, sentence or numbers to convert from text to Morse Code (including spaces between words): "; //ASK USER FOR SPECIFIC INFORMATION
	getline(cin, in, '\n'); // includes blank spaces.

	int len = in.length(); // get length of string.

	for (int i = 0; i<len; i++) {
		char letter = in[i]; // get it character from string.
		cout << "letter " << letter; // display character
		morseCode(letter); // convert to Morse code sound and dot-dash print
		cout << endl; // skip a line on output
		Sleep(1000); // wait (about) 1ooo milliseconds
	}
	return 0;
} // end of main
  // INPUT: character
  // OUTPUT: Morse Code sounds and dot-dash print
void morseCode(char letter) // ALL ALPHABECTIC LETTERS(A-Z) AND NUMBERS FROM 0 TO 9
{
	switch (toupper(letter)) { // change character into its Morse code sounds.

	case 'A': //ADD EVERY ALPHABETIC LETTERS
		dot(); dash();
		break;

	case'B':
		dash(); dot(); dot(); dot();
		break;

	case 'C':
		dash(); dot(); dash(); dot();
		break;

	case 'D':
		dash(); dot(); dot();
		break;
	case 'E':
		dot();
		break;

	case'F':
		dot(); dot(); dash(); dot();
		break;

	case 'G':
		dash(); dash(); dot();
		break;

	case 'H':
		dot(); dot(); dot(); dot();
		break;

	case 'I':
		dot(); dot();
		break;

	case'J':
		dot(); dash(); dash();dash();
		break;

	case 'K':
		dash(); dot(); dash();
		break;

	case 'L':
		dot(); dash(); dot(); dot();
		break;

	case 'M':
		dash(); dash();
		break;

	case 'N':
		dash(), dot();
		break;

	case 'O':
		dash(); dash(); dash();
		break;

	case 'P':
		dot(); dash(); dash(); dot();
		break;

	case 'Q':
		dash(); dash(); dot(); dash();
		break;

	case'R':
		dot(); dash(); dot();
		break;

	case 'S':
		dot(); dot(); dot();
		break;

	case 'T':
		dash();
		break;

	case 'U':
		dot(); dot(); dash();
		break;

	case'V':
		dot(); dot(); dot(); dash();
		break;

	case 'W':
		dot(); dash(); dash();
		break;

	case 'X':
		dash(); dot(); dot(); dash();
		break;

	case 'Y':
		dash(); dot(); dash(); dash();
		break;

	case'Z':
		dash(); dash(); dash(); dot();
		break;

	case ' ':
		// pause without sound.
		break;

	case '0': //NUMBERS FROM 0 TO 9
		dash(); dash(); dash(); dash(); dash();
		break;

	case '1':
		dot(); dash(); dash(); dash(); dash();
		break;

	case '2':
		dot(); dot(); dash(); dash(); dash();
		break;

	case '3':
		dot(); dot(); dot(); dash(); dash();
		break;

	case '4':
		dot(); dot(); dot(); dot();
		break;

	case '5':
		dot(); dot(); dot(); dot(); dot();
		break;

	case '6':
		dash(); dot(); dot(); dot(); dot();
		break;

	case '7':
		dash(); dash(); dot(); dot(); dot();
		break;

	case '8':
		dash(); dash();dash(); dot(); dot();
		break;

	case '9':
		dash(); dash();dash(); dot();
		break;

	default:
		cout << "bad input" << "Please enter a setence, words (A-Z) or numbers (0-9) to translate" endl; //ASK USER AGAIN FOR INPUT

	}

}


 // end of Morse code

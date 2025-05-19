# CIS279-Project-3-solution

Download Here: [CIS279 Project #3 solution](https://jarviscodinghub.com/assignment/cis279-project-3-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Our project is the development of a miniature text-editing program. This program will allow only a few simple commands and is, therefore, quite primitive in comparison with a modern text editor or word processor. Even so, it illustrates some of the basic ideas involved in the construction of much larger and more sophisticated text editors.

The Node Class
Chapter 5 of your text introduced a Node class and linked list toolkit of functions that could be used to create and maintain a singly linked list using this class. I have provided a version of this class and toolkit functions. You are to add five functions to this toolkit (prototypes to the .h file, function definitions to the .cpp file ).

void list_tail_remove(node*& headptr);
// Effect: The tail (last) node has been removed and returned to the heap;
// headptr is the head pointer of the new, shorter linked list.
// Precondition: headptr is the head pointer of a linked list (list has at least one node)

void list_tail_insert(node*& headptr, const node::value_type& entry);
// Effect: A new node containing the given entry has been added at
// the tail of the linked list; headptr points to the head of the new,
// longer linked list.
// Precondition: headptr is the head pointer of a linked list (list may be empty)

node* getLast(node* headptr)
// Effect: finds the last node in the list
// Precondition: headptr is the head pointer of a linked list with at least one node
// Returns: a pointer to the last node in the list

void outNode(ostream& out, const node* headPtr)
// Effect: prints the data contains in node pointed to by headPtr to output stream ‘out’

void outList(ostream& out, const node* headPtr)
//Precondition: list may be empty
//Effect: prints the data contained in a linked list. headPtr points to the 1st node of list.

You will want to code a simple driver to make sure that these functions work correctly before you go on. The driver can simply create a linked list and then call the functions verifying that they work. Test functions with empty lists where applicable. This driver is not to be handed in, but to help you (the final application is easier to debug if you are already assured that this class functions correctly).

The LineEditor class

A LineEditor object stores the contents of a textfile, and allows simple editing of the file. The textfile contents are stored as a collections of strings. There is always a ‘current line’ number stored. You are to implement the LineEditor class using a linked list of strings, and an int currentLine as the two member variables (other member variables if you want, although not necessary)

Functions for LineEditor class:

Effect: LineEditor object is created
Postcondition: no strings are in the list (the list is empty). Current line is 0.
LineEditor::LineEditor()

Effect: LineEditor object initialized with data
Precondition: name is a ifstream object for a file that HAS BEEN SUCCESSFULLY OPENED
Postcondition: Lines from the file have been stored in the linked list (one line per node). The
current line has been set to the first line (if the file is empty, current line is 0)
void LineEditor::fill(ifstream& name)

Effect: determines the number of lines stored in the file
Precondition: None
Postcondition: object is unchanged
Returns: the number of lines in the file
int LineEditor::numLines()

Effect: access function for current line number
Precondition: None
Postcondtion: object is unchanged
int LineEditor::currentLine()

Effect: prints the current line to the filestream ‘out’; if object is empty, prints “No Lines Stored”
Precondition: None
Postcondition: object is unchanged
void LineEditor:: printCurrent(ostream& out)

Effect: adds new first line
Precondition: None
Postcondition: a new line has been added prior to existing lines
The current line has been reset to the first line (ie. 1)
void LineEditor::insertFirst(string line)

Effect: adds new last line
Precondition: None
Postcondition: a new line has been added following existing lines
The current line has been reset to the last line
void LineEditor::insertLast(string line)

Effect: adds a new line following the current line
Precondition: list is not empty
Postcondition: a new line has been inserted preceding the current line. The current
line number does not change
void LineEditor::insertCur (string line)

Effect: deletes the first line
Precondition: the exists 1 or more line in the file
Postcondition: the first line has been removed. The current line is now the new
first line. If there are no line remaining, the current line is 0.
void LineEditor::delFirst()

Effect: deletes the last line
Precondition: there is at least one line
Postcondition: the last line has been removed. The current line has been reset to
the new last line. If there are no lines remaining, the current line is set to 0.
void LineEditor::delLast()

Effect: deletes the current line
Precondition: list is not empty
Postcondition: the current line has been removed. If there are no more lines, the
current line is set to 0.
void LineEditor::delCur()

Effect: finds the first occurrence of a substring within the file
Precondition: None
Postcondition: If the substring was found, the current line has been changed to
the line in which that substring occurred
Returns: true if substring was found, false otherwise
bool LineEditor::findStr(const string& str)

Effect: replaces first occurrence of substring ‘old’ with substring ‘new’ in current line
Precondition: current line is not 0
Postcondition: current line may have been updated (if old occurred in line)
void LineEditor::replaceStr(const string& old, const string& new)

Effect: prints out contents of LineEditor, each line separated by \n
Precondition: None
Postcondition: LineEditor object is unchanged
friend ostream& operator<<(ostream& out, const LineEditor& obj) The Application You are to write a simple text editor, which does the following: 1.) Asks the user for the name of file to be edited. If that file cannot be opened, the program gives a message and exits. 2.) Creates a LineEditor object and then fills that object with text from the file 3.) Allows the user to choose any of the following options, until he/she wants to exit • Allows the user to print out the entire file to the screen • Allows the user to print out the current number and current line to the screen • allows the user to add a new first line to the file • allows the user to add a new last line to the file • allows the user to insert a new line as current line • allows the user to delete the first line • allows the user to delete the last line • allows the user to delete the current line • allows the user to find the first occurrence in file of a substring • allows the user to replace one string from current line with another • allows the user to print out the number of lines in the file Your program should print the current line following the processing of each user choice. 4.) Once the user has chosen to exit, the file is written back be sure you have closed the input file, then reopen it for output. (You may want to use a separate file for output until you are sure your program works.) Submit your updated Node.h, Node.cpp, LineEditor.h, LineEditor.cpp and application file via email attachment (grassos@smccd.edu). You do not need to zip the files.

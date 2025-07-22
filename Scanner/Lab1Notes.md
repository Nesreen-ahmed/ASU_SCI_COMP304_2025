# Compiler Lab1 : Scanner

## :open_book: Read File c++


 ### 1 ) Read by Line

	#include <fstream> //Include the Required Header
	#include <iostream> 
	#include <string> // For reading lines into a string

	using namespace std;
	void readLineByLine(string inputFile)
	{
	    ifstream inFile(inputFile); // Declare a variable to handle file operations and Opens the file for reading
	    if (!inFile.is_open()){ // check if the file open or not
	        cout << "Error opening file!" << endl;
        return; // Indicate an error
		}
		string line;
		while (getline(inFile, line)) {  // Read the file line-by-line into the variable 'line'
			cout << line << endl;  //do your task
		}
		inFile.close();
    }

 ### 2 ) Read by Word

		#include <fstream>
		#include <iostream> 
		#include <string> 

		using namespace std;
		void readWordByWord(string inputFile)
		{
		    ifstream inFile(inputFile);
		    if (!inFile.is_open()){
		        cout << "Error opening file!" << endl;
	        return; 
	        }

			string word;  
			while (inFile >> word) {  // Read the file word-by-word into the variable 'word'
				cout << word << endl;  
			}
			inFile.close();
	    }
### 3 ) Read by Char

			#include <fstream>
			#include <iostream> 
			#include <string> 

			using namespace std;
			void readCharByChar(string inputFile)
			{
			    ifstream inFile(inputFile);
			    if (!inFile.is_open()){
			        cout << "Error opening file!" << endl;
		        return; 
		        }

				char ch;  
				while (inputFile.get(ch)) { // Read the file char-by-char into the variable 'ch' 
					cout << ch;  
				}
				inFile.close();//close file
		    }
---
## :writing_hand: Write in File C++

			#include <fstream>
			#include <iostream> 
			#include <string> 

			using namespace std;
			void writeInFile(string outputFile)
			{
			    ofstream outFile(outputFile);  // Declare a variable to handle file operations and Opens the file for reading and Opens the file for writing 
			    if (!outFile.is_open()){
			        cout << "Error opening file!" << endl;
		        return;
		        }

				outFile << "1234" << endl;
				outFile << "Number" << endl;  

				outFile.close();
		    }
---
## :mag: Comparison of Set, Vector, and Map in C++ (Runtime Complexity)

| **Operation**          | **set** (Balanced BST) | **vector** (Dynamic Array) | **map** (Balanced BST) |
|------------------------------------|--------------------------------|----------------------------|------------------------------------|
| **Insertion**          | `O(log n)`                 | `O(1)` (amortized at end), `O(n)` (middle) | `O(log n)`       |
| **Deletion**           | `O(log n)`                 | `O(1)` (end), `O(n)` (middle)              | `O(log n)`       |
| **Search (find)**      | `O(log n)`                 | `O(n)` (linear search)                     | `O(log n)`       |
| **Access by key**      | `O(log n)`                 |  Not applicable (use index)                | `O(log n)`       |
| **Access by index**    | Not supported              | `O(1)` (random access)                     | Not supported    |
| **Sorting**            | Always sorted              | `O(n log n)`(`std::sort`)                  | Always sorted by key |

---
## :pushpin: Some Tips

 - **Give functions and variables names that indicate what they do. This makes your code easier to understand and more readable.**
 - **Break the task into smaller tasks and then solve them**
 - **ex :**
   - In a scanner, you need to know the next state at each step, so you can build a function that returns nextState(currentState, char) instead of writing more lines to do that step. This makes your code more readable.
 - **Again, Write your own code!**
 - **Feel free to ask in the WhatsApp group and discuss your problem and idea**
---
## :link: References

  - [Vector](https://www.geeksforgeeks.org/cpp/vector-in-cpp-stl/)
  - [Set](https://www.geeksforgeeks.org/cpp/set-in-cpp-stl/)
  - [ForEachLoop](https://www.geeksforgeeks.org/cpp/g-fact-40-foreach-in-c-and-java/)
  - [Map](https://www.geeksforgeeks.org/cpp/map-associative-containers-the-c-standard-template-library-stl/)
  - [MAP_of_MAP](https://www.geeksforgeeks.org/cpp/implementing-multidimensional-map-in-c/)

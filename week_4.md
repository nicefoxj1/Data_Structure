# Array & Dynamic Allocation

## 1. Dynamic Allocation 
### - Example 1 (allocation & free)
```C++
# include <iostream>
using namespace std;

int glo = 1; // Global Variable

void main() {

	int loc = 2; // Local Variable
	int *ptr = new int; // Pointer allocation
	*ptr = 3;
	

	cout << glo << endl;
	cout << loc << endl;
	cout << *ptr << endl;
	

	// Free Variables
	delete ptr;
	delete &glo; // Doesn't work
	delete &loc; // Doesn't work
}
```

### - Example 2 (dynamic allocate & set values & free)
```C++
#include <iostream>
using namespace std;

void main() {
	int *list;
	int arr_size;

	// Input array size
	cout << "* Set Size" << endl;
	cout << "Array size : ";
	cin >> arr_size;

	// Allocate & Set values
	list = new int[arr_size];

	cout << "* Set Variables" << endl;
	for (int i = 0; i < arr_size; i++) {
		cout << i << "'th element : ";
		cin >> list[i];
	}

	// Print contents of pointer
	cout << endl << "* Print Variable" << endl;
	for (int i = 0; i < arr_size; i++) {
		cout << "List[" << i << "]=" << list[i] << endl;
	}

	delete[] list;
}
```

## 2. 2D Array
### - Example 1
```C++
#include <iostream>
using namespace std;

int main() {
	int i32cnt = 1;
	int array2D[3][4];

	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 4; j++) {
			array2D[i][j] = i32cnt;
			i32cnt++;
		}
	}
	cout << *array2D[0] << "\t" << array2D[0] << endl;
	cout << *array2D[1] << "\t" << array2D[1] << endl;
	cout << *array2D[2] << "\t" << array2D[2] << endl;

}
```

## 3. 2D Array using Pointer
### - Example 1
```C++
#include <iostream>
using namespace std;

int main() {
	int i32cnt = 1;
	int *array2D[3];

	for (int i = 0; i < 3; i++) {
		array2D[i] = new int[4];
		for (int j = 0; j < 4; j++) {
			array2D[i][j] = i32cnt;
			i32cnt++;
		}
	}

	cout << *array2D[0] << "\t" << array2D[0] << endl;
	cout << *array2D[1] << "\t" << array2D[1] << endl;
	cout << *array2D[2] << "\t" << array2D[2] << endl;

	for (int i = 0; i < 3; i++) {
		delete[] array2D[i];
	}
}
```

### - Example 2
```C++
#include <iostream>
using namespace std;

int main() {
	int i32cnt = 1;
	int *array2D[3];

	for (int i = 0; i < 3; i++) {
		array2D[i] = new int[4];
		for (int j = 0; j < 4; j++) {
			array2D[i][j] = i32cnt;
			i32cnt++;
		}
	}

	cout << *array2D[0] << "\t" << array2D[0] << endl;
	cout << *array2D[1] << "\t" << array2D[1] << endl;
	cout << *array2D[2] << "\t" << array2D[2] << endl;

	cout << *(array2D[0] + 1) << "\t" << array2D[0] + 1 << endl;
	cout << *(array2D[0] + 2) << "\t" << array2D[0] + 2 << endl;
	cout << *(array2D[0] + 3) << "\t" << array2D[0] + 3 << endl;

	for (int i = 0; i < 3; i++) {
		delete[] array2D[i];
	}
}

```

## 4. 2D Array using Double Pointer
### - Example 1
```C++
#include <iostream>
using namespace std;

int main() {
	int i32cnt = 1;
	int **array2D;
	array2D = new int *[3];

	for (int i = 0; i < 3; i++) {
		array2D[i] = new int[4];
		for (int j = 0; j < 4; j++) {
			array2D[i][j] = i32cnt;
			i32cnt++;
		}
	}

	cout << *array2D[0] << "\t" << array2D[0] << endl;
	cout << *array2D[1] << "\t" << array2D[1] << endl;
	cout << *array2D[2] << "\t" << array2D[2] << endl;

	cout << *(array2D[0] + 1) << "\t" << array2D[0] + 1 << endl;
	cout << *(array2D[0] + 2) << "\t" << array2D[0] + 2 << endl;
	cout << *(array2D[0] + 3) << "\t" << array2D[0] + 3 << endl;

	for (int i = 0; i < 3; i++) {
		delete[] array2D[i];
	}
	delete[] array2D;
}
```

### TASK (1)
```C++

/*
  Write Down your Code
*/

```

### TASK (2)
```C++
#include <iostream>
#include <stdlib.h>

using namespace std;

void print_function(char **arr, int i) {

	cout << "Array [" << i << "] saved " << arr[i] << endl;
}

void main() {
	int n;
	char **name;
	char name_input[20];
	cout << "Number of people : ";
	cin >> n;

	// Array name is allocated by user's number
	/*
		Write Down your Code
	*/

	
	for (int i = 0; i < n; i++) {
		cout << "name : ";
		/*
		
		Write Down your Code
		
		*/
	}
}

```



# Basic C++ 2

## 1. Inline function
### - Example 1-1
```C++
#include <iostream>
#define SQUARE(x) ((x)*(x))
using namespace std;

int main(void)
{
	cout << SQUARE(5) << endl;
	return 0;
}
```

```C++
#include <iostream>
using namespace std;

int main(void)
{
	cout << ((5) * (5)) << endl;
	return 0;
}
```

### - Example 1-2
```C++
#include <iostream>
using namespace std;

inline int SQUARE(int x)
{
	return x * x;
}
int main(void)
{
	cout << ((5) * (5)) << endl;
	return 0;
}
```
### - Example 2
```C++
#include <iostream>
using namespace std;

inline int SQUARE(int x)
{
	return x * x;
}
int main(void)
{
	cout << ((5) * (5)) << endl;
	return 0;
}
```

## 2. Pointer & Reference
### - Example 1-1
```C++
#include <iostream>
using namespace std;

int main(){
  int num = 50;
  int &num1 = num;
  
  cout << "num : " << &num <<endl;
  cout << "num1 : " << &num1 << endl;
  
	return 0;
}
```

### - Example 1-2
```C++
#include <iostream>
using namespace std;

int main(){
  int num = 50;
  int &num1 = num;
  int &num2 = num;
  int &num3 = num2;
  
  cout << "num : " << &num <<endl;
  cout << "num1 : " << &num1 << endl;
  cout << "num2 : " << &num2 << endl;
  cout << "num3 : " << &num3 << endl;
  
	return 0;
}
```
### - Example 2-1
```C++
void  swap(int* a, int* b) {
	int temp;
	temp = *a;
	*a = *b;
	*b = temp;
}
int main(void) {
	int a = 10, b = 20;
	swap(&a, &b);
	cout << a << b << endl;
	return 0;
}
```
### - Example 2-2
```C++
void  swap(int* a, int* b) {
	int temp;
	temp = *a;
	*a = *b;
	*b = temp;
}
int main(void) {
	int a = 10, b = 20;
	swap(&a, &b);
	cout << a << b << endl;
	return 0;
}
```

## 3. Constructor & Destructor

```C++

class Vector {
private:
	int x;
	int y;
public:
	Vector(int _x, int _y);  // constructor 
	~Vector();
	Vector operator+(Vector vec);
	Vector operator*(int mag);
	void print_coord(void);
};
Vector::Vector(int _x, int _y)
{
	cout << "constructor called" << endl;
	x = _x;
	y = _y;
}
Vector::~Vector()
{
	cout << "destructor called" << endl;
}
Vector Vector::operator+(Vector vec)
{
	return Vector(this->x + vec.x, this->y + vec.y);
}
Vector Vector::operator*(int mag)
{
	return Vector(this->x * mag, this->y * mag);
}
```
### - Example 1-1
```C++
int main(void)
{
	Vector a(1, 1);
	Vector b(1, 2);

	return 0;
}
```
### - Example 1-2
```C++
int main(void)
{
	Vector a(1, 1);
	Vector b(1, 2);

	a.print_coord();
	b.print_coord();

	Vector c = a + b;
	Vector d = a * 3;

	c.print_coord();
	d.print_coord();

	return 0;
}
```

### - Task 1
```C++
class Vector {
  /*
  
    write down your own code
  
  */
}
```C++
int main(void)
{
	Vector a(1, 1);
	Vector b(1, 2);

	c = a - b;
	c.print_coord();

	d = a / 3;
	d.print_coord();

	return 0;
}
```

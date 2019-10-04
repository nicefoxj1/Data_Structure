# Basic C++ 1

## 1. C++
### - Example 1
```C++
#include <iostream>
#include <cstring>
using namespace std;

int myfunc(int a) { return 0; }

int myfunc(int a, int b)
{
	return 0;
}

int myfunc(int num = 7)
{
	return num;
}
int main(void)
{
	double num1;
	double num2;

	cout << "enter first number";
	cin >> num1;
	
}
int main(void)
{

	char* str = (char*)malloc(sizeof(char) * 20);
	strcpy(str, "hello");
	cout << str << endl;
	free(str);

	int* ptr1 = new int;
	delete ptr1
}
```
### - Example 2
```C++
typedef double newdouble;

namespace ProgComImp1
{
	int simpleFunc(void)
	{return 0;}
}
namespace BestComImp1
{
	int simpleFunc(void)
	{
		return 0;
	}
}
```
### - Example 3
```C++
typedef double newdouble;
namespace Aspace
{
	void func(newdouble num)
	{
		cout << "This is A space and number is "
			<< num << endl;
	};
	void func(newdouble num1, newdouble num2)
	{
		cout << "This is A space and number is " << num1 <<
			" and " << num2 << endl;
	}
}
namespace Bspace
{
	void func(newdouble num=3)
	{
		cout << "This is B space and number is " <<
			num << endl;
	};
	void func(newdouble num1, newdouble num2)
	{
		cout << "This is B space and number is " <<
			num1 << " and " << num2 << endl;
	}
}
int main(void)
{
	double num1;
	double num2;

	cout << "enter first number ";
	cin >> num1;

	cout << "enter second number ";
	cin >> num2;

	Aspace::func(num1);
	Aspace::func(num1, num2);

	Bspace::func();
	Bspace::func(num1);
	Bspace::func(num1, num2);

	return 0;
}
```
## 2. OOP
## 3. Class
### -Task 1
```C++
#include <iostream>
#include <cstring>
using namespace std;

class Bird{
private:
	char name[30];
	int age;
public:
	void print_age(void);
	// declaration inside the class
	void print_name(void) {
		cout << age << endl;
	};
	void set_age(int);
	void set_name(char*);
};

// declaration outside the class
void Bird::print_age(void) {
	cout << name << endl;
};

void Bird::set_age(int _age) {
	/* Write down your own code */
}

void Bird::set_name(char*_name){
	strcat_s(name,_name);
}
*/
int main(void) {
  /* Write down your own code */
}
```

## 4. Abstraction
### - Example 1
```C++
class Younghee {
private:
	char name[30];
	int age;
public:
	void print_age(void);
	void print_name(void);
	void set_age(int);
	void set_name(char*);
};
class Chulsoo {
private:
	char name[30];
	int age;
public:
	void print_age(void);
	void print_name(void);
	void set_age(int);
	void set_name(char*);
};

int main(void) {
	Younghee younghee;
	Chulsoo chulsoo;
}
```

```C++
class Person {
private:
	string name;
	int age;
public:
	void print_age(void);
	void print_name(void);
	void set_age(int);
	void set_name(string);
};
void Person::print_age(void) {
	cout << age << endl;
}
void Person::print_name(void) {
	cout << name << endl;
}
void Person::set_age(int _age) {
	age = _age;
}
void Person::set_name(string _name) {
	name = _name;
}
int main(void) {
	Person Younghee;
	Person Chulsoo;
}
```

## 5. Encapsulation
### - Example 1
```C++
class Person {
private:
	string name;
	int age;
public:
	void print_age(void);
	void print_name(void);
	void set_age(int);
	void set_name(string);
};
void Person::print_age(void) {
	cout << age << endl;
}
void Person::print_name(void) {
	cout << name << endl;
}
void Person::set_age(int _age) {
	age = _age;
}
void Person::set_name(string _name) {
	name = _name;
}
int main(void) {
	Person Younghee;
	Person Chulsoo;

	string name = "Younghee";
  Younghee.set_name(name);

	// try to run this!
	cout << Younghee.name << endl;
	// didnt work? then try this
	Younghee.print_name();
}
```

## 6. Inheritance
### - Example 1
```C++

class Empolyee :public Person {
private:
	string company;
	double salary;
public:
	void input_company(string _company_name, double _salary);
	void get_employ_info(void);
};
void Empolyee::input_company(string _company_name, double _salary){
	company = _company_name;
	salary = _salary;
}
void Empolyee::get_employ_info(void) {
	cout << "company is " << company << endl;
	cout << "salary is " << salary << endl;
}

int main(void) {
	Empolyee Younghee;

	string name = "Younghee";
	Younghee.set_name(name);
	Younghee.input_company("TI", 100);

	// didnt work? then try this
	Younghee.print_name();
	Younghee.get_employ_info();

}

```

## 7. Polymorphism
### - Example 1
```C++
class parent {
public:
	virtual void house(void) { cout << "parent's house" << endl; }
};

class child : public parent
{
public:
	void house(void) { cout << "child's house" << endl; }
};

int main(void) 
{
	parent* pp = new parent();
	child* cc = new child();
	parent* pc = new child();

	pp->house();
	cc->house();
	pc->house();
}
```

### Task 3
```C++
/*

  Write Down your own Code

*/

int main(void)
{
	Dog* dog = new Dog();
	Cat* cat = new Cat();
	Animal* ani = new Animal();

	Animal* ani2 = new Dog();

	dog->say();
	cat->say();
	ani->say();

	ani2->say();
	
	return 0;
}
```

# Karina Punko

### Contact
email: punko.karina@yandex.by
<br/>
tel: +375-(029)-662-47-64(vel)

### Summary
I studying in BSUIR on budget on FIK(now i started the 2nd course).In the programm of the 1st year we had programming on C++ and also course of web-programming( HTML/CSS JS and PHP CMS like Wordpress). I enjoed that year and at this summer had acquaintance with Opencart CMS. I like programming and what to conect my life with Frontend development.Now i can't say that i know JS on cool level, but i try to be the best of me and develop my skills with this courses.
### Skills
- C++,OOP
- HTML/CSS
### Code examples
This part from my course work connected with OOP on C++
/////PolyClass.h
```sh
class PolyClass
{
public:
int degree;
int *coef;
// d-макс степень c-коэфициент
PolyClass(int d);
~PolyClass();
PolyClass(PolyClass &t);// t-обьект второй
CString operator+(PolyClass &t);
CString operator-(PolyClass &t);
CString operator*(PolyClass &t);
CString set_value_x(int x);
void inputarray(int *arr);
CString output();
};

```
///PolyClass.cpp
```sh
#include "pch.h"
#include "PolyClass.h"
#include <iostream>
#include <string>
using namespace std;

PolyClass::PolyClass(int d)
{
degree = d;
coef = new int[d + 1];
for (int i = 0; i <= d; i++)
coef[i] = 0;
}

PolyClass::PolyClass(PolyClass&t)
{
degree = t.degree;
coef = new int[degree + 1];
for (int i = 0; i <= degree; i++)
coef[i] = t.coef[i];
}
PolyClass::~PolyClass()
{
delete[]coef;
}
CString PolyClass::operator+(PolyClass &t)
{
if (degree >= t.degree)
{
PolyClass temp(degree);
for (int i = 0; i <= t.degree; i++)
temp.coef[i] = coef[i] + t.coef[i];
for (int i = t.degree + 1; i <= degree; i++)
temp.coef[i] = coef[i];
return temp.output();
};
if (degree < t.degree)
{
PolyClass temp(t.degree);
for (int i = 0; i <= degree; i++)
temp.coef[i] = coef[i] + t.coef[i];
for (int i = degree + 1; i <= t.degree; i++)
temp.coef[i] = t.coef[i];
return temp.output();
};
}
CString PolyClass::operator-(PolyClass &t)
{
if (degree >= t.degree)
{
PolyClass temp(degree);
for (int i = 0; i <= t.degree; i++)
temp.coef[i] = coef[i] - t.coef[i];
return temp.output();
}
else {
PolyClass temp(t.degree);
for (int i = 0; i <= degree; i++)
temp.coef[i] = coef[i] - t.coef[i];
for (int i = degree + 1; i <= t.degree; i++)
temp.coef[i] = -t.coef[i];
return temp.output();
}
}
CString PolyClass::operator*(PolyClass &t)
{
PolyClass temp(degree + t.degree);
for (int i = 0; i <= degree; i++)
{
for (int j = 0; j <= t.degree; j++)
temp.coef[i + j] += coef[i] * t.coef[j];
}
return temp.output();
}

CString PolyClass::set_value_x(int x) {
string result;
int resultint = 0;
for (int i = 0; i < degree + 1; i++) {
resultint += coef[i] * pow(x, i);
};
result.append(to_string(resultint));
return CString(result.c_str());
};
void PolyClass::inputarray(int *arr) {
coef = arr;
}
CString PolyClass::output()
{
string string="";
int b = degree;
string.append(to_string(coef[b])).append("x^").append(to_string(b));
b = b - 1;
for (int i =b; i > 0; i--)
{
if (coef[i] < 0) { string.append(to_string(coef[i])); };
if(coef[i]>0){
string.append("+").append(to_string(coef[i]));
};
if (coef[i] != 0) {
string.append("x^").append(to_string(i));
};

};
if (coef[0] < 0) string.append(to_string(coef[0]));
if (coef[0] > 0) string.append("+").append(to_string(coef[0]));
return CString(string.c_str());
}
```
### Experience
I wrote app for polynomial and also do different lab works at universite.
there are my document which contain my work(doc in Russian language).
### Education
I studying in BSUIR on budget on FIK.Also I have attended various free course platforms such as: [htmlacademy](https://htmlacademy.ru/study), [code-basics](https://ru.code-basics.com/), [yandexpr.paktikum](https://praktikum.yandex.ru/web)
### English
In my opinion I had solid Intermediate level. I can speak pretty good and have good vocabulary for usual situations,but had problems with grammar.



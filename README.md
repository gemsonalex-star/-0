اول مشروع صغير لي سنه اولى فصل اول//
//2  AL WAFAA! 2026/3/2 THIS MY FERST YEAR IN C++ PRO !

#include<iostream>
#include<cmath>
#include<iomanip>
#include <unordered_map>

using namespace std;

void Format() { cout << fixed << setprecision(5); }

double Perimetersquare(double side) {return 4 * side;}
double Areasquare(double side) {return side * side;}
double Diagonalsquare(double side) { return side* sqrt(2);}

double PerimeterRectangle(double length, double width) {return 2 * (length + width);}
double AreaRectangle(double length, double width) { return width * length; }
double DiagonalRectangle(double length, double width) {return sqrt((width * width) + (length * length)); }

double CircumferencCircle(double R) {  return 2 * 3.141592653589793 * R; }
double AreaCircle(double R) { return 3.141592653589793 * R * R; }


double AreaEquilatearlTriangle(double side) { return (sqrt(3) / 4) * (side * side); }
double PerimeterEquilatearlTriangle(double side) { return 3 * side; }
//متساوي الساقين
double AreaIsoscelesTriangle(double side, double base) { return (0.5) * (base * (sqrt((side * side) - ((base / 2) * (base / 2))))); }
double PerimeterIsoscelesTriangle(double side, double base) { return (2 * side) + base; }
//مختلف الاضلاع
double PerimeterScaleneTriangle(double a , double b, double c) { return a + b + c; }
double AreaScaleneTriangle(double a, double b, double c){ double p = (a + b + c) / 2; return sqrt(p * (p - a) * (p - b) * (p - c)); }
//قائم
double PerimeterRightTriangle(double a, double b){ double c = sqrt((a * a) + (b * b)); return a + b + c; }
double AreaRightTriangle(double a, double b) { return (0.5)* (a * b); }
double HypotenuseRightTriangle(double a, double b ){return sqrt((a * a) + (b * b)); }
//حساب نوع المثلث
int Detectrtangletype(double a, double b, double c) {
	if (a + b <= c || a + c <= b || b + c <= a) return 0;
	if (a == b && b == c)return 1;
	if (a == c || a == b || b == c)return 2;
	if (a * a + b * b == c * c || a * a + c * c == b * b || c * c + b * b == a * a)return 4;
	if (a != b && c != a && b != c) return 3;}
//حساب أطوال الأرتفاعات
//مختلف الاضلاع
double HeightscaleneA(double a, double b, double c) { double A = AreaScaleneTriangle(a, b, c); return (2 * A) / a; }
double HeightscaleneB(double a, double b, double c) { double A = AreaScaleneTriangle(a, b, c); return (2 * A) / b; }
double HeightscaleneC(double a, double b, double c) { double A = AreaScaleneTriangle(a, b, c); return (2 * A) / c; }
//قائم
double HeightRightA(double a, double b) { return b; }
double HeightRightB(double a, double b) { return a; }
double HeightRightC(double a, double b,double c) { return (b*a)/c; }
//متساوي الساقين
double HeightIsoscelesTriangleC(double a, double c ) { return sqrt((a * a) - ((c / 2) * (c / 2))); }
double HeightIsoscelesTriangleA(double a, double c) {double h_c = HeightIsoscelesTriangleC(a, c); return (c * h_c) / a;}
double HeightIsoscelesTriangleB(double a, double c) {return HeightIsoscelesTriangleA(a, c);}
//متساوي الاضلاع
double HeightEquilatearlTriangle(double side) { return (sqrt(3) / 2) * (side); }
//لوغاريتم
double  NaturalLogarithm2(double num) { return log(num); }
double  CommonLogarithm10(double num) { return log10(num); }
double  BinaryLogarithm(double num) { return log(num)/log(2); }
//أسي
double  Exponential(double num){ return exp(num); }
//زوايا
//تحويل للراديان
double RadToDeg(double rad) {return rad * 180.0 / 3.141592653589793;}
//توابع مثاثية
double TrigonometricFunctionsS(double angle) { return sin(angle); }
double TrigonometricFunctionsC(double angle) { return cos(angle); }
double TrigonometricFunctionsT(double angle) { return tan(angle); }
//زائدية
double HyperbolicS(double x) { return sinh(x); }
double HyperbolicC(double x) { return cosh(x); }
double HyperbolicT(double x) { return tanh(x); }
//نصوص
void choic1() {
	cout << "=============CHOICE=================\n";
	cout << "Do you want to start this program!? \n";
	cout << "1-FOR Geometric Shapes.\n";
	cout << "2-FOR Mathematical Calculations.\n";
	cout << "3-FOR Conversions.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic2() {
	cout << "=============CHOICE===========\n";
	cout << "1-FOR Squares & FOR Rectangle.\n";
	cout << "2-FOR Circle.\n";
	cout << "3-FOR Triangle.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic3(){
	cout << "=============CHOICE===========\n";
	cout << "1-FOR Squares.\n";
	cout << "2-FOR Rectangle.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic4(){
	cout << "=============CHOICE===========\n";
	cout << "1-FOR Preimeter && Area.\n";
	cout << "2-FOR Diagonal\n ";
	cout << "ENTER YOUR CHOICE : ";
}
void choic5(){
	cout << "=============CHOICE===========\n";
	cout << "1-FOR Circumferenc && Area.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic6(){
	cout << "=============CHOICE===========\n";
	cout << "1-For Perimeter and Area.\n";
	cout << "2-For Heights.\n";
	cout << "3-For Hypotenuse.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic7(){
	cout << "=============CHOICE===========\n";
	cout << "1-FOR Logarithm and Exponential(e^x).\n";
	cout << "2-Angle Functions.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic8(){
	cout << "=============CHOICE===========\n";
	cout << "1-Logarithm .\n";
	cout << "2-Exponential.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic9(){
	cout << "=============CHOICE===========\n";
	cout << "Choose Logarithm Type:\n";
	cout << "1-Natural Logarithm(ln).\n";
	cout << "2-Common Logarithm(log10).\n";
	cout << "3-Binary Logarithm(log2).\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic10(){
	cout << "=============CHOICE===========\n";
	cout << "1-Trigonometric Functions.\n";
	cout << "2-Hyperbolic .\n";
	cout << "3-Inverse Trigonometric Functions.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void choic11(){
	cout << "=============CHOICE===========\n";
	cout << "1-For Lengthو Weight Time.\n";
	cout << "ENTER YOUR CHOICE : ";
}
void please(){
	cout << "=============PLEASE===========\n";

	cout << "*Please  enter your choice again*\n ";
}
void walcome(){
	cout << "================================== \n";
	cout << "==========\"WALCOME AGAIN!\"=========== \n";
	cout << "================================== \n";
}
void thank(){
	cout << "===========================================================================================\n";
	cout << " ****Thank you for using the Geometry Master. Precision is always one calculation away.****\n";
	cout << "===========================================================================================\n";
}
void continu(){
	cout << "=============================================================================\n";
	cout << " DO you want to continue (1)==>YES (0)==>NO ?\n";
}
void input(){ 
	cout << "=============INPUT=================\n";
}
void Result(){ 
	cout << "=============RESULT=================\n"; 
}
int main()
{
	system("color 1F");
	cout << "*******************************Welcome to the Geometry master - Where precision meets power!***************************\n";
	int goo = 1;
	while (goo == 1) {
		int go;
		choic1();
		cin >> go;
		if (go == 1) {
			while (go == 1) {
				int choice;
				choic2();
				cin >> choice;
				if (choice == 1)
				{
					while (choice == 1) {
						int k;
						choic3();
						cin >> k;
						if (k == 1) {
							while (k == 1) {
								int x;
								choic4();
								cin >> x;
								if (x == 1)
								{
									double rib;
									input();
									cout << "Enter Side length :    ";
									cin >> rib;
									Result();
									Format();
									cout << "Result FOR  Preimeter = " << Perimetersquare(rib) << endl;
									Result();
									cout << "Result FOR Area = " << Areasquare(rib) << endl;
								}
								else if (x == 2)
								{
									double rib;
									input();
									cout << "Enter Side length :    ";
									cin >> rib;
									Result();
									Format();
									cout << "Result FOR Diagonal = " << Diagonalsquare(rib) << endl;
								}
								else
								{
									
									please();
									continue;
								}
								break;
							}
						}
						else if (k == 2)
						{
							while (k == 2) {
								double length;
								double width;
								int x;
								choic4();
								cin >> x;
								if (x == 1)
								{
									input();
									cout << "Enter width :";
									cin >> width;
									cout << "Enter length : ";
									cin >> length;
									Format();
									Result();
									cout << "Result FOR Preimeter  = " << PerimeterRectangle(length, width) << endl;
									Result();
									cout << "Result FOR Area = " << AreaRectangle(length, width) << endl;
								}
								else if (x == 2)
								{
									input();
									cout << "Enter width :";
									cin >> width;
									cout << "Enter length : ";
									cin >> length;
									Format();
									Result();
									cout << "Result FOR Diagonal = " << DiagonalRectangle(length, width) << endl;
								}
								else {
									
									please();
									continue;
								}
								break;
							}
						}
						else {
							
							please();
							continue;
						}
						break;
					}
				}
				else if (choice == 2)
				{
					while (choice == 2) {
						int g;
						choic5();
						cin >> g;
						if (g == 1) {
							double  R;
							input();
							cout << "Enter Radius :\n";
							cin >> R;
							Format();
							Result();
							cout << "Result FOR Circumferenc = " << CircumferencCircle(R) << endl;
							Result();
							cout << "Result FOR Area = " << AreaCircle(R) << endl;
						}
						else
						{
							
							please();
							continue;
						}
						break;
					}
				}
				else if (choice == 3)
				{
					while (choice == 3) {

						int tchoice;
						choic6();
						cin >> tchoice;
						if (tchoice == 1) {
							double a, b, c;
							input();
							cout << "Enter side c FOR (Hypotenuse OR Base) : ";
							cin >> c;
							cout << "Enter side a: ";
							cin >> a;
							cout << "Enter side b: ";
							cin >> b;
							int type = Detectrtangletype(a, b, c);
							switch (type) {
							case 0:
								cout << "This is NOT a valid triangle.\n";
								break;
							case 1:
								Result();
								cout << "Triangle Type: Equilateral\n";
								Format();
								cout << "Perimeter = " << PerimeterEquilatearlTriangle(a) << endl;
								cout << "Area = " << AreaEquilatearlTriangle(a) << endl;
								break;
							case 2:
								Result();
								cout << "Triangle Type: Isosceles\n";
								Format();
								cout << "Perimeter = " << PerimeterIsoscelesTriangle(a, c) << endl;
								cout << "Area = " << AreaIsoscelesTriangle(a, c) << endl;
								break;
							case 3:
								Result();
								cout << "Triangle Type: Scalene\n";
								Format();
								cout << "Perimeter = " << PerimeterScaleneTriangle(a, b, c) << endl;
								cout << "Area = " << AreaScaleneTriangle(a, b, c) << endl;
								break;
							case 4:
								Result();
								cout << "Triangle Type: Right Triangle\n";
								Format();
								cout << "Hypotenuse = " << HypotenuseRightTriangle(a, b) << endl;
								cout << "Perimeter = " << PerimeterRightTriangle(a, b) << endl;
								cout << "Area = " << AreaRightTriangle(a, b) << endl;
								break;
							}
						}
						else if (tchoice == 2)
						{
							double a, b, c;
							input();
							cout << "Enter side c FOR (Hypotenuse OR Base) : ";
							cin >> c;
							cout << "Enter side a: ";
							cin >> a;
							cout << "Enter side b: ";
							cin >> b;
							int type = Detectrtangletype(a, b, c);
							switch (type) {
							case 0:
								cout << "This is NOT a valid triangle.\n";
								break;
							case 1:
								Result();
								cout << "Triangle Type: Equilateral\n";
								Format();
								cout << "Height = " << HeightEquilatearlTriangle(a) << endl;
								break;
							case 2:
								Result();
								cout << "Triangle Type: Isosceles\n";
								Format();
								cout << "Height on side C = " << HeightIsoscelesTriangleC(a, c) << endl;
								cout << "Height on side A = " << HeightIsoscelesTriangleA(a, c) << endl;
								cout << "Height on side B = " << HeightIsoscelesTriangleB(a, c) << endl;
								break;
							case 3:
								Result();
								cout << "Triangle Type: Scalene\n";
								Format();
								cout << "Height on side A = " << HeightscaleneA(a, b, c) << endl;
								cout << "Height on side B = " << HeightscaleneB(a, b, c) << endl;
								cout << "Height on side C = " << HeightscaleneC(a, b, c) << endl;
								break;
							case 4:
								Result();
								cout << "Triangle Type: Right Triangle\n";
								Format();
								cout << "Height on side A = " << HeightRightA(a, b) << endl;
								cout << "Height on side B = " << HeightRightB(a, b) << endl;
								cout << "Height on side C = " << HeightRightC(a, b, c) << endl;
								break;
							}
						}
						else if (tchoice == 3) {
							double a, b;
							input();
							cout << "Enter side a: ";
							cin >> a;
							cout << "Enter side b: ";
							cin >> b;
							Format();
							Result();
							cout << "Hypotenuse =" << HypotenuseRightTriangle(a, b) << endl;
						}
						else {
							
							please();
							continue;
						}
						break;
					}
				}
				else {
					
					please();
					continue;
				}
				break;
			}
		}
		else if (go == 2) {
			while (go == 2)
			{

				int l;
				choic7();
				cin >> l;
				if (l == 1)
				{
					while (l == 1) {
						int e;
						choic8();
						cin >> e;
						if (e == 1)
						{
							while (e == 1) {
								int l1;
								choic9();
								cin >> l1;
								if (l1 == 1) {
									double num;
									input();
									cout << "enter your numper :\n";
									cin >> num;
									Format();
									Result();
									cout << "Result FOR Natural Logarithm " << num << "=" << NaturalLogarithm2(num) << endl;
								}
								else if (l1 == 2) {
									double num;
									input();
									cout << "enter your numper :\n";
									cin >> num;
									Format();
									Result();
									cout << "Result FOR Common Logarithm " << num << "=" << CommonLogarithm10(num) << endl;
								}
								else if (l1 == 3) {
									double num;
									input();
									cout << "enter your numper :\n";
									cin >> num;
									Format();
									Result();
									cout << "Result FOR Binary Logarithm " << num << "=" << BinaryLogarithm(num) << endl;
								}
								else {
									
									please();
									continue;
								}
								break;
							}
						}
						else if (e == 2) {
							double num;
							input();
							cout << "enter your numper :\n";
							cin >> num;
							Format();
							Result();
							cout << "Result FOR Exponential" << num << "=" << Exponential(num) << endl;
						}
						else {
							
							please();
							continue;
						}
						break;
					}
				}
				else if (l == 2)
				{
					while (l == 2) {
						int s;
						choic10();
						cin >> s;
						if (s == 1) {
							double angleDegrees;
							input();
							cout << "Enter angle in degrees:\n";
							cin >> angleDegrees;
							double angleRadians = angleDegrees * (3.141592653589793 / 180.0);
							Format();
							Result();
							cout << "sin(" << angleDegrees << "°) = " << TrigonometricFunctionsS(angleRadians) << endl;
							cout << "cos(" << angleDegrees << "°) = " << TrigonometricFunctionsC(angleRadians) << endl;
							cout << "tan(" << angleDegrees << "°) = " << TrigonometricFunctionsT(angleRadians) << endl;
						}
						else if (s == 2) {
							double num;
							input();
							cout << "Enter value for hyperbolic functions:\n";
							cin >> num;
							Format();
							Result();
							cout << "sinh(" << num << "°) = " << HyperbolicS(num) << endl;
							cout << "cosh(" << num << "°) = " << HyperbolicC(num) << endl;
							cout << "tanh(" << num << "°) = " << HyperbolicT(num) << endl;
						}
						else if (s == 3) {
							double x;
							input();
							cout << "Enter angle in numper:\n";
							cin >> x;
							if (x >= -1.0 && x <= 1.0) {
								cout << "asin(" << x << "):\n";
								Format();
								Result();
								cout << "  radians = " << asin(x) << endl;
								cout << "  degrees = " << RadToDeg(asin(x)) << endl;
							}
							else
							{
								cout << "asin(" << x << ") is undefined (x must be between -1 and 1)\n";
							}
							if (x >= -1.0 && x <= 1.0) {
								cout << "acos(" << x << "):\n";
								Format();
								Result();
								cout << "  radians = " << acos(x) << endl;
								cout << "  degrees = " << RadToDeg(acos(x)) << endl;
							}
							else
							{
								cout << "acos(" << x << ") is undefined (x must be between -1 and 1)\n";
							}
							cout << "atan(" << x << "):\n";
							Format();
							Result();
							cout << "  radians = " << atan(x) << endl;
							cout << "  degrees = " << RadToDeg(atan(x)) << endl;
						}
						else {
							
							please();
							continue;
						}
						break;
					}

				}
				else {
					
					please();
					continue;
		}
				break;
			}
			}
else if (go==3){
	while (go ==3 ) {

		int z;
		choic11();
		cin >> z;
		if (z == 1) {
			while (true) {
				unordered_map<string, double> tos = {
					{"s", 1.0},
					{"min",60.0},
					{"h",3600.0},
					{"d",86400.0},
					{"wk",604800}
				};
				unordered_map<string, double> toMeter = {
		  {"mm", 0.001},
		  {"cm", 0.01},
		  {"m", 1.0},
		  {"km", 1000.0},
		  {"in", 0.0254},
		  {"ft", 0.3048},
		  {"yd", 0.9144},
		  {"mi", 1609.34}
				};
				unordered_map<string, double> tokg = {
  {"mg", 0.000001},
  {"g", 0.001},
  {"kg", 1.0},
  {"t", 1000.0},
  {"oz", 0.0283495},
  {"lb", 0.453592},
  {"st", 6.35029}
				};

				double value;
				string unit;
				input();
				cout << "Enter value and unit (e.g. 10 cm OR g OR min): ";
				cin >> value >> unit;

				if (toMeter.find(unit) != toMeter.end()) {
					double result = value * toMeter[unit];
					Result();
					cout << value << " " << unit << " = " << result << " m" << endl;
					break;
				}
				else if (tokg.find(unit) != tokg.end()) {
					double result = value * tokg[unit];
					Result();
					cout << value << " " << unit << " = " << result << " kg" << endl;
					break;
				}
				else if (tos.find(unit) != tos.end()) {

					double result = value * tos[unit];
					Result();
					cout << value << " " << unit << " = " << result << " " << endl;
					break;
				}
				else {
					cout << "Unknown unit!" << endl;
					continue;
				}
			}
			break;
		}
		else {
			please();
			continue;
		}
}
}
else {
	please();
	continue;
}
        continu();
		cin >> go;
		if (go == 1)
		{
			system("cls");
			walcome();
			continue;
		}
		else
		{
			system("cls");
			thank();
			break;
		}
	}
	return 0;
}

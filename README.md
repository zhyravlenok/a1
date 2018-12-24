#include "stdafx.h"
#include <iostream> 
#include <conio.h> 
#include <stdio.h> 
#include <fstream> 
#include <string> 
#include <stdlib.h> 

using namespace std;


void Mat()
{
	char ch = 100;
	while (ch != 27)
	{
		system("cls");
		cout << "***Математика***\n";
		cout << "1. Тема 1\n";
		cout << "2. Тема 2\n";
		cout << "3. Тема 3\n";
		cout << "4. Вернуться\n";
		cout << ">: ";
		ch = _getch();
		//if (ch == 49) 
		//if (ch == 50) 
		//if (ch == 51) 
		if (ch == 52) ch = 27;
	}
}

void Bio()
{
	char ch = 100;
	while (ch != 27)
	{
		system("cls");
		cout << "***Биология***\n";
		cout << "1. Тема 1\n";
		cout << "2. Тема 2\n";
		cout << "3. Тема 3\n";
		cout << "4. Вернуться назад\n";
		cout << ">: ";
		ch = _getch();
		//if (ch == 49) 
		//if (ch == 50) 
		//if (ch == 51)
		if (ch == 52) ch = 27;
	}
}

void Ist()
{
	char ch = 100;
	while (ch != 27)
	{
		system("cls");
		cout << "***История***\n";
		cout << "1. Тема 1\n";
		cout << "2. Тема 2\n";
		cout << "3. Тема 3\n";
		cout << "4. Вернуться назад\n";
		cout << ">: ";
		ch = _getch();
		//if (ch == 49) 
		//if (ch == 50) 
		//if (ch == 51)
		if (ch == 52) ch = 27;
	}
}

void Ruk()
{
	char ch = 100;
	while (ch != 27)
	{
		system("cls");
		cout << "***Информации по работе программы***\n";
		cout << "Информация какая-то\n";
		cout << "Чтобы вернуться назад нажмите любую главишу 1\n";
		cout << ">: ";
		ch = _getch();
		if (ch == 49) ch = 27;
	}
}

void Start()
{
	char ch = 100;
	while (ch != 27)
	{
		system("cls");
		cout << "***Предметы***\n\n";
		cout << "**Выберите предмет**\n";
		cout << "1. Математика\n";
		cout << "2. Биология\n";
		cout << "3. История\n";
		cout << "4. Просмотр информации по работе программы \n";
		cout << "5. Выйти из программы\n";
		cout << ">: ";
		ch = _getch();
		if (ch == 49) Mat();
		if (ch == 50) Bio();
		if (ch == 51) Ist();
		if (ch == 52) Ruk();
		if (ch == 53) ch = 27;
		
	}
}


void Menu()
{
	char ch = 100;
	{
		ofstream File("XXX.txt", ios_base::out);
		string Name, Name1, Name2;
		float group;
		cout << "Введите ФИО(через пробел)\n";
		cout << "Ввод >:"; cin >> Name >> Name1 >> Name2; File << Name << Name1 << Name2;
		cout << "Введите группу\n";
		cout << "Ввод >:"; cin >> group; File << group;
		cout << "\nДля продолжение нажмите любую главишу";
		ch = _getch();
		Start();
	}
}


int main()
{
	system("chcp 1251>>null");
	//setlocale(0, "rus");
	Menu();
    return 0;
}

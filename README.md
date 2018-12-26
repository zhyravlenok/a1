#include "stdafx.h"
#include <iostream> 
#include <conio.h> 
#include <stdio.h> 
#include <fstream> 
#include <string> 
#include <stdlib.h> 
#include <iostream> 
#include <filesystem> 


using namespace std;
namespace fs = experimental::filesystem;


void Mat()
{
	char ch = 100;
	while (ch != 27)
	{
		system("cls");
		cout << "***Математика***\n";
		string path = "../предметы/1. Математика";
		for (auto & p : fs::directory_iterator(path))
			cout << p << endl;
		cout << "4. Вернуться\n";
		cout << ">: ";
		ch = _getch();
		//if (ch == 49) Mat();
		//if (ch == 50) Bio;
		//if (ch == 51) Ist
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
		string path = "../предметы/2. Биология";
		for (auto & p : fs::directory_iterator(path))
			cout << p << endl;
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
		string path = "../предметы/3. История";
		for (auto & p : fs::directory_iterator(path))
			cout << p << endl;
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
		string path = "../предметы";
		for (auto & p : fs::directory_iterator(path))
			cout << p << endl;
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
	Menu();
    return 0;
}

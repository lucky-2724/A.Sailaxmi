# A.Sailaxmi#
#this project explains how we can book a ticket for n number of passangers from the given list #
#include<iostream>
using namespace std;
#include<iomanip>
#include<windows.h>
#include<string.h>
class x
{
	public:

		int get()
		{	
			cout<<"\t\t\t[1]Booking ticket:"<<"\t\t\t"<<"[3]Cancel ticket"<<endl;
			cout<<"\t\t\t\t\t\t[2]PNR check"<<endl;
		
		}	
};
class y:public x
{	
		string S1,S2,mail;int d,b,age;	int amount,p;long long num;	string name,g;	string t;
	public:
		int dis();
		int dis1();
		int dis2();
		int get2();
		int get3(int);
		int get6(int,int);
		int dis3();
		int get4(int);
		int get5(int,int);
		int get1()
		{
			int a,n;
	
			cin>>a;
		switch (a)
		{
			case 1: dis();
					break;
			case 2: cout<<"your ticket was cancelled";
					break;
			case 3: cout<<"Invalid PNR";
				    break;
			default: cout<<"PLEASE ENTER THE GIVEN NUMBERS";
					 break;
				}
		}
};
int y::dis()
{	
	int n;
		cout<<"please enter no. of passengers:";
			cin>>n;	
		return (n);
	
}
int y::get2()
{

	
	cout<<"Name:";
	cin>>name;
	cout<<"age:";
	cin>>age;
	cout<<"Gender:";
	cin>>g;
}
int y::get3(int n)
{

		cout<<setw(15)<<"Starting Point:";
		cin>>S1;
		cout<<setw(13)<<"Destination Point:";
		cin>>S2;
		cout<<"DATE OF JOURNEY(ddmmyyyy):";
		cin>>d;
		cout<<setw(35)<<"  AVALIABLE TRAINS:"<<endl;
	 	cout<<setw(45)<<">>[1]. rajadhani express:(2.00AM)"<<endl;
	 	cout<<setw(45)<<">>[2]. Humsafur sf express:(10.00AM)"<<endl;
		cout<<setw(45)<<">>[3]. shatabdhi express:(3.00PM)"<<endl;
		cout<<setw(45)<<">>[4]. kerala express:(8.00PM)"<<endl;
		cin>>b;
		get6(b,n);
	}
	int y::get6(int b,int n)
	{
	
			switch (b)
		{
			case 1: cout<<setw(30)<<"your are booking for rajadhani ->enter personal details:"<<endl;
					t="rajadhani";
					get4(n);
					break;
			case 2: cout<<setw(30)<<"your are booking for Humsafur ->enter personal details:"<<endl;
					t="Humsafur";
					break;
					get4(n);
			case 3: cout<<setw(30)<<"your are booking for shatabdhi ->enter personal details:"<<endl;	
					t="shatabdhi EX";
					get4(n);
					break;
			case 4: cout<<setw(30)<<"your are booking for kerala ->enter personal details:"<<endl;
					t="kerala EX";
					get4(n);
					break;
			default: cout<<"please select the given number:"<<endl;		
		}
	}
		int y::get4(int n)
		{
			int c;
			cout<<"\n[1]>>apply coupon:(10%)"<<endl;
		cout<<"[2]>>paramilitary forces:(40%)"<<endl;
		cout<<"[3]>>railway employees:(40%)"<<endl;
		cout<<"[4]>>please press 4 not to apply any coupon(0%)"<<endl;
		cin>>c;
		get5(c,n);
		}
		int y::get5(int c,int n)
		{
			
			int p;
			switch(c)
		{
			case 1: p=600*0.1;
					amount=(600-p)*n;
					break;
			case 2: p=600*0.4;
					amount=(600-p)*n;
					break;
			case 3: p=600*0.4;
					amount=(600-p)*n;
					break;
			case 4: amount=600*n;
					break;
		}
		cout<<"phone number:";
		cin>>num;
		cout<<"enter Email Id:";
		cin>>mail;
		cout<<"[1]->print ticket:"<<endl;
		cout<<"[2]->you want to Reset:"<<endl;
		cout<<"\t\t\t Your Ticket"<<endl;
		cin>>p;
		}
		int y::dis1()
		{
			cout<<"\t\tName:"<<name;
			cout<<"\t\t\t\tage:"<<age;
			cout<<"\t\t\t\t\t\tGender:"<<g<<endl;
		}
int y::dis3()
{
	cout<<"\t\t\tphone number:"<<num;
	cout<<"\t\t\t\tmail:"<<mail<<endl;
	cout<<"\t\t\tStarting point:"<<S1;
	cout<<"\t\t\t\tEnding point:"<<S2<<endl;
	cout<<"\t\t\tTrain:"<<t;
	cout<<"\t\t\t\tyour coach is B4"<<endl;
	cout<<"\t\t\tAmount:"<<amount;
	cout<<"\t\t\t\tPNR no.=7095591217"<<endl;

	
}
int y::dis2()
{	int m;long long pnr;
	cout<<"[1] check PNR:"<<endl;
	cout<<"[2] Cancel Ticket:"<<endl;
	cin>>m;
	if(m==1)
	{
		cout<<"enter 10digit pnr no.:" ;
		cin>>pnr;
		if(pnr==7095591217)
		{
			cout<<"your ticket is available:";
			dis3();
		}
		else
		{
			cout<<"invalid pnr:";
		}
	}
	else
	{
		cout<<"tickect cancelled"<<endl;
		
	}
}
int main()
{
	system("COLOR 05");
	int i,k,a,n;
	y obj,obj1[10];
	obj.get();
	n=obj.get1();
	for(i=0;i<n;i++)
	{
		obj1[i].get2();
	}
	obj.get3(n);
		for(i=0;i<n;i++)
	{
		obj1[i].dis1();
	}

	obj.dis3();
	obj.dis2();

}

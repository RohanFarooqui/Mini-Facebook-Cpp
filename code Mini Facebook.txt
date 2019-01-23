#include <iostream>
#include <string.h>
#include <fstream>
#include <stdlib.h>
#include <stdio.h>
#include <cstdlib>
#include <time.h>
#include <string>
#include <windows.h>
#include <conio.h>
#include <dos.h>
#include <direct.h>
#include <stdio.h>
using namespace std;

class mfb
{
 private:
        string first_name;
        string sur_name;
        string email_address;
        string mobile_num;
        string password;
        string dob;
        string sex;
        string k;
		string current_dir;
 public:
    mfb(){
         first_name= "Anonymous";
         sur_name= "Anonymous";
         email_address= "Anonymous@anonymous.com";
         password= "1234";
         dob= "01-01-2000";
         sex= "FM";
         k= "k";}
	void acc_info(){
        ofstream fout;
        fout.open("User_info.txt",ios::app);
        system("cls");
        cout<<"**********Create an Account*********** "<<endl;
        cout<<"          ----------------            "<<endl;
        cout<<"Enter First Name : ";
        cin.ignore();
        getline(cin,first_name);
        cout<<"Enter Sur Name : ";
        //cin.ignore();
        getline(cin,sur_name);
        cout<<"Enter Email address : ";
        //cin.ignore();
        //getline(cin,email_address);
        cin>>email_address;
        cout<<"Enter Mobile Number : ";
        cin>>mobile_num;
        cout<<"Enter Password : ";
        //cin.ignore();
        cin>>password;
        cout<<"Enter Date of Birth (DD/MM/YY): ";
        cin.ignore();
        getline(cin,dob);
        cout<<"For Male press M or press F for Female : ";
        cin>>sex;
        cout<<"Creating Your Account ";
        for (int j = 0; j < 5; j++) {cout<<" ";
        for (int i = 0; i < 5; i++) {cout << ".";
        Sleep(300);}}
        cout<<"Your Account is Successfully Created"<<endl;
        fout<<first_name<<" "<<sur_name<<" "<<mobile_num<<" "<<email_address<<" "<<password<< " " <<dob << " "<<sex <<" "<<endl;
        CreateDirectory (("E:/Mini FB/User_Data_base/"+first_name).c_str(), NULL);

        fout.close();
        system("cls");
}

};
class login_account : public mfb
{
 private:
     string ph;
     string pswd;
     string name;
     string Date_of_Birth;
     string emailaddress;
     string gender;
     string s;
     string comment;
     string fr;
     string address;
     string page_name;
     string block_person;
     string friend_fb;
     string path;
     string page;
     string friend_request;
     string n;
     string arr;
     string group[5];
     string block[400];
     string str1,str2,str3,str4,str5,str6,str7;
     string new_name;
     string paragraph;
     string rohan;
     int option;
     int x;
     int newsfeeds;
     int pages;
     int opt;
     char square[10] = {'o','1','2','3','4','5','6','7','8','9'};
     int player = 1,i,choice;
     char mark;


 public:
    login_account(){
     string ph;
     string pswd;
     string name;
     string Date_of_Birth;
     string emailaddress;
     string gender;
     string s;
     string comment;
     string fr;
     string address;
     string page_name;
     string block_person;
     string friend_fb;
     string path;
     string page;
     string friend_request;
     string n;
     string arr;
     string group[5];
     string block[400];
     string str1,str2,str3,str4,str5,str6,str7;
     string new_name;
     string paragraph;
     string rohan;
     int option;
     int x;
     int newsfeeds;
     int pages;
     char square[10] = {'o','1','2','3','4','5','6','7','8','9'};
     int player = 1,i,choice;
     char mark;
     int opt;}

   int login_acc(){
         jug:
         ifstream readFile;
         readFile.open("User_info.txt", ios::in);
         bool flag;
         system("cls");
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<" "<<endl;
         cout<<"                          "<<"Enter Your Mobile Number or Email Address : ";
         cin>>ph;
         cout<<"                          "<<"Enter Your Account Password : ";
         cin>>pswd;
         while(!readFile.eof()){
            readFile>>str1>>str2>>str3>>str4>>str5>>str6>>str7;
            if((ph == str3 || ph == str4) && pswd == str5){
                  flag = true;
                  break;}
            else{
                  flag = false;
                  continue;}}
            if(flag == true){
          cout<<" "<<endl;
          cout<<"                          "<<"You are successfully Login Into Your Account"<<endl;
          cout<<"                          "<<"Logging into Your Account";
                          for (int j = 0; j < 2; j++) {cout<<" ";
                          for (int i = 0; i < 2; i++) {cout << ".";
                          Sleep(300);}}
                          system("cls");
                          goto jun;}
         else{cout<<"Mail Address or Password is Incorrect!!!"<<endl;
              cout<<"Try again"<<endl;
              goto jug;}//readFile.close()
        jun:
        cout<<" "<<endl;
        cout<<"Welcome : " <<str1 << " " <<str2 <<endl;
        ff:
        cout<<"                                         "<<"\n"<<endl;
        cout<<"                                         "<<"*============Plz Choose a Option==================*"<<endl;
        cout<<"                                         "<<"|-> Press (1)  To Show News Feeds                 |"<<endl;
        cout<<"                                         "<<"|-> Press (2)  To Post something on Your TimeLine |"<<endl;
        cout<<"                                         "<<"|-> Press (3)  To Send Friend Request             |"<<endl;
        cout<<"                                         "<<"|-> Press (4)  To Like a Page                     |"<<endl;
        cout<<"                                         "<<"|-> press (5)  People You may Know                |"<<endl;
        cout<<"                                         "<<"|-> Press (6)  To Create Group                    |"<<endl;
        cout<<"                                         "<<"|-> Press (7)  To Block a friend                  |"<<endl;
        cout<<"                                         "<<"|-> Press (8)  To Show Friends                    |"<<endl;
        cout<<"                                         "<<"|-> Press (9)  To Show Groups                     |"<<endl;
        cout<<"                                         "<<"|-> Press (10) To Show Followers                  |"<<endl;
        cout<<"                                         "<<"|-> Press (11) To Show Mutual Friends             |"<<endl;
        cout<<"                                         "<<"|-> Press (12) To Show Family Members             |"<<endl;
        cout<<"                                         "<<"|-> Press (13) To Show Pages You like             |"<<endl;
        cout<<"                                         "<<"|-> Press (14) To Play Game                       |"<<endl;
        cout<<"                                         "<<"|-> Press (15) To Show Your Time-line             |"<<endl;
        cout<<"                                         "<<"|-> Press (16) To Show Block List                 |"<<endl;
        cout<<"                                         "<<"|-> Press (17) To Logout                          |"<<endl;
        cout<<"                                         "<<"*##############################################*"<<endl;
        cout<<"                                         "<<"################################################"<<endl;
        cout<<"                                         "<<"Choose an Option To see Further : ";
        cin>>option;
        if(option == 1){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            cout<<"*********************************************************************"<<endl;
            cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
            cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
            cout<<"|Mobile No: "<<str3<<endl;
            cout<<"*********************************************************************"<<endl;
            cout<<"====================================================================="<<endl;
            cout<<" "<<endl;
            cout<<"\n"<<"News Feeds : "<<endl;
            cout<<" "<<endl;
            ifstream in;
            address=(("E://Mini FB///Files loaded for options//news_feeds.txt"));
            in.open(address.c_str());
            while(!in.eof()){
                getline(in,s);
                cout<<s<<"\n";}
                in.close();
            newsfee:
            cout<<" "<<endl;
            cout<<"###########################"<<endl;
            cout<<"#-> Press (1) for like    #"<<endl;
            cout<<"#-> Press (2) for Comment #"<<endl;
            cout<<"#-> Press (3) for Share   #"<<endl;
            cout<<"#-> Press (4) exit        #"<<endl;
            cout<<"###########################"<<endl;
            cin>>newsfeeds;
            if(newsfeeds == 1){cout<<" ^-> " <<endl;goto newsfee;}
            else if(newsfeeds == 2){cout<<"Enter Comment : ";
                                    cin>>comment;
                                    cout<<str1<<" "<<str2<<" "<<":"<< comment <<endl; goto newsfee;}
            else if(newsfeeds == 3){cout<<"The post is Share "<<endl; goto newsfee;}
            else if(newsfeeds == 4){goto jun;}}
        if(option == 2){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            ofstream out;
            path=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\posts.txt"));
            out.open(path.c_str(),ios::app);
            cout<<" "<<endl;
            cout<<"Write something to Post on your Timeline....... : "<<endl;
            cin.ignore();
            getline(cin,paragraph);
            out<<paragraph<<endl;
            cout<<"\n Posting on Your Time line : ";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            out.close();}
        if(option == 3){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            cout<<"\n"<<"Enter the Name of Person You want to  add as a friend :";
            cin.ignore();
            getline(cin,friend_request);
            cout<<"The Friend Request is Send to : " <<friend_request <<endl;
            ofstream out;
            path=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\friends.txt"));
            out.open(path.c_str(),ios::app);
            out<<friend_request<<endl;
            cout<<"Saving Changes : ";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            out.close();}
        if(option == 4){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            cout<<"\n"<<"Pages List : "<<endl;
            cout<<" "<<endl;
            ifstream in;
            address=(("E://Mini FB//Files loaded for options//Pages Names.txt"));
            in.open(address.c_str());
            while(!in.eof()){
                getline(in,s);
                cout<<"->"<<s<<endl;}
            cout<<"\n"<<"Enter the Name of Page You like : ";
            cin.ignore();
            getline(cin,page);
            ofstream out;
            path=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\pagelike.txt"));
            out.open(path.c_str(),ios::app);
            out<<page<<endl;
            cout<<"Saving Changes : ";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);
            in.close();}}}
        if(option == 5){
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"People You may Know : "<<endl;
           ifstream in;
           address=(("E://Mini FB//Files loaded for options//people_you_may_know.txt"));
           in.open(address.c_str());
           for(int i=1 ; i<= 10;i++){
                x = rand() %31;
                getline(in,s);
                cout<<i<<")"<<" "<<s;
                cout<<" ";
                if(i == 5)cout<<endl;}
                cout<<endl;
                in.close();}
         if(option == 6){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            ofstream out;
            path=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\groups.txt"));
            out.open(path.c_str(),ios::app);
            cout<<"Group making";
            cout<<"You can Enter  5 persons in a Group : "<<endl;
            cout<<"Enter the name of Group : ";
            cin.ignore();
            getline(cin,n);
            out<<"Group Name:" << n <<endl;
            cout<<"\n Enter the name of People You want to add in group : ";
            for(int i=1 ; i<=5 ; i++){
                cin>>group[i];}
            for(int i=1 ; i<=5 ; i++){
            out<<"->" <<group[i]<<endl;}
            cout<<"Saving Changes : ";
            for (int j = 0; j < 3; j++) {cout<<" ";
            for (int i = 0; i < 3; i++) {cout << ".";
            Sleep(300);}}
            out.close();}
        if(option == 7){
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"Blocked People : "<<endl;
           cout<<"Enter the Name of Person You want to Block : ";
           cin.ignore();
           getline(cin,s);
           ofstream out;
           address=(("E://Mini FB//User_Data_base//" + str1 + "//blockedpeople.txt"));
           out.open(address.c_str(),ios::app);
           out<<"->"<<s<<endl;
           cout<<"\n Adding Person in Blocking List : ";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           out.close();}
        if(option == 8){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            cout<<"*********************************************************************"<<endl;
            cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
            cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
            cout<<"|Mobile No: "<<str3<<endl;
            cout<<"*********************************************************************"<<endl;
            cout<<"====================================================================="<<endl;
            cout<<" "<<endl;
            cout<<"All Friends : "<<endl;
            int count=0;
            ifstream in;
            address=(("E://Mini FB//User_Data_base//" + str1 + "//friends.txt"));
            in.open(address.c_str(), ifstream::in | ifstream::binary);
            in.seekg(0,ios::end);
            int filesize = in.tellg();
            if(filesize == 0 || !in){cout<<"There Are No friends in Your Account "<<endl;}
            else{
             while(!in.eof()){
                getline(in,s);
                cout<<"->"<<s<<endl;
                count++;}}
           in.close();
           cout<<"Total Number of Friends : " << count <<endl;
           cout<<"Closing File : ";
           for (int j = 0; j < 3; j++) {cout<<" ";
           for (int i = 0; i < 3; i++) {cout << ".";
           Sleep(300);}} }
       if(option == 9){
            system("cls");
            cout<<"Loading Groups : ";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            ifstream in;
            path=(("E://Mini FB//User_Data_base//" + str1 + "//groups.txt"));
            in.open(path.c_str());
            cout<<" "<<endl;
            cout<<"Groups in Your Account : "<<endl;
            while(!in.eof()){
                getline(in,s);
                cout<<s<<endl;}
            cout<<"Closing File  : ";
            for (int j = 0; j < 3; j++) {cout<<" ";
            for (int i = 0; i < 3; i++) {cout << ".";
            Sleep(300);}}
            in.close();}
       if(option == 10){
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"Followers : "<<endl;
           ifstream in;
           address=(("E://Mini FB//Files loaded for options//followers.txt"));
           in.open(address.c_str());
           for(int i=1 ; i<= 10;i++){
                x = rand() %2943;
                getline(in,s);
                cout<<i<<")"<<" "<<s;
                cout<<" ";
                if(i == 5)cout<<endl;}
                cout<<endl;
           cout<<"Closing File : ";
           for (int j = 0; j < 3; j++) {cout<<" ";
           for (int i = 0; i < 3; i++) {cout << ".";
           Sleep(300);}}
           in.close();}
       if(option == 11){
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"Mutual Friends : "<<endl;
           ifstream in;
           address=(("E://Mini FB//User_Data_base//" + str1 + "//friends.txt"));
           in.open(address.c_str());
           if(!in){cout<<"There Are No Mutual friends in Your Account "<<endl;}
           else{
             while(!in.eof()){
                getline(in,s);
                cout<<"#>"<<s<<endl;}
           cout<<"Closing File : ";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           in.close();}}
        if(option == 12){
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"Family Members : "<<endl;
           ifstream in;
           address=(("E://Mini FB//User_Data_base//" + str1 + "//friends.txt"));
           in.open(address.c_str());
           if(!in){cout<<"There Are No Family Members in Your Account "<<endl;}
           else{
           for(int i=1 ; i<= 10;i++){
                while(!in.eof()){
                getline(in,s);
                cout<<"->"<<s;
                cout<<" ";
                if(i == 5)cout<<endl;}}
           cout<<"\nClosing ...."<<endl;
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           in.close();}}
        if(option == 13){
            cout<<"Loading";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);}}
            system("cls");
            cout<<"\n Pages List : "<<endl;
            cout<<" "<<endl;
            ifstream in;
            address=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\pagelike.txt"));
            in.open(address.c_str());
            if(!in){cout<<"There are No Pages You like "<<endl;}
            else{
               while(!in.eof()){
                 getline(in,s);
                 cout<<"->"<<s<<endl;}
            in.close();}
            cout<<"Closing : ";
            for (int j = 0; j < 2; j++) {cout<<" ";
            for (int i = 0; i < 2; i++) {cout << ".";
            Sleep(300);
            }}}
        if(option == 14){
           system("cls");
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           cout<<" "<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"###################################"<<endl;
           cout<<"#-> Press(1) for Guess Number Game#"<<endl;
           cout<<"#-> Press(2) for Tic Tak Toe      #"<<endl;
           cout<<"#-> Press(3) for Exit             #"<<endl;
           cout<<"###################################"<<endl;
           cout<<"Enter Your Choice : ";
           cin>>opt;
           if(opt == 1){
                system("cls");
                cout<<"Loading";
                for (int j = 0; j < 2; j++) {cout<<" ";
                for (int i = 0; i < 2; i++) {cout << ".";
                Sleep(300);}}
                system("cls");
                random_game();}
           else if(opt == 2){
                system("cls");
                cout<<"Loading";
                for (int j = 0; j < 2; j++) {cout<<" ";
                for (int i = 0; i < 2; i++) {cout << ".";
                Sleep(300);}}
                system("cls");
                tictak();}
           else if(opt == 3){goto jun;}
           }
        if(option == 15){
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           cout<<"Time Line : "<<endl;
           ifstream in;
           path=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\posts.txt"));
           in.open(path.c_str());
           if(!in){cout<<"Nothing is posted yet :)  "<<endl;}
           else{
             while(!in.eof()){
                getline(in,s);
                cout<<s<<endl;}
           in.close();}
           }
        if(option == 16){
           cout<<"Loading";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           system("cls");
           cout<<"*********************************************************************"<<endl;
           cout<<"|Name : "<<str1<<" "<<str2<<"                             "<<"Email ID : "<<str4<<endl;
           cout<<"|Gender : "<<str7<<"                                          "<<"Date_of_Birth : "<<str6<<endl;
           cout<<"|Mobile No: "<<str3<<endl;
           cout<<"*********************************************************************"<<endl;
           cout<<"====================================================================="<<endl;
           cout<<" "<<endl;
           ifstream in;
           address=(("E:\\Mini FB\\User_Data_base\\" + str1 + "\\blockedpeople.txt"));
           in.open(address.c_str());
           if(!in){cout<<"NO Person is Blocked by You" <<endl;}
           else{
               cout<<"Blocked People : "<<endl;
               while(!in.eof()){
                  getline(in,s);
                  cout<<s<<endl;}
           in.close();}
           cout<<"/n closing : ";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}}
        if(option == 17){
           system("cls");
           cout<<"Logging you out";
           for (int j = 0; j < 2; j++) {cout<<" ";
           for (int i = 0; i < 2; i++) {cout << ".";
           Sleep(300);}}
           cout<<"\n"<<"Have Nice Day : " << str1 <<" "<<str2 <<endl;
           cout<<"You are Logged out from Your account"<<endl;
           exit(0);}
           goto ff;}
       void random_game(){
           system("cls");
           cout<<"   " <<endl;
           cout<<"                                    "<<"##########   Number Guess Game   #######"<<endl;
           cout<<" "<<endl;
           cout<<"                                    "<<"#############  Instructions   ##########"<<endl;
           cout<<"        "<<"Note:"<<endl;
           cout<<"                "<<"In  this game a number is generate you only have ONE tries to Guess  "<<endl;
           cout<<"                "<<"number.If Number is Guess than you have to guess further three times" <<endl;
           int n;
           int r = rand()% 10;
           cout<<"Enter Your Name : ";
           cin>>name;
           cout<<"Guess number between 1 & 10 :";
           cin>>n;
           while(true ){
             if(n==r){cout<<"Perfect Guess "<<" "<<name<<" :) GOOD JOB!!! "; break;}
             else{cout<<"Wrong Guess :(( Try Next Time !!"; break;}}}

      int tictak(){
	         do{
		        board();
		        player=(player%2)?1:2;
		        cout << "Player " << player << ", enter a number:  ";
		        cin >> choice;
		        mark=(player == 1) ? 'X' : 'O';
		        if (choice == 1 && square[1] == '1')square[1] = mark;
		        else if (choice == 2 && square[2] == '2')square[2] = mark;
		        else if (choice == 3 && square[3] == '3')square[3] = mark;
		        else if (choice == 4 && square[4] == '4')square[4] = mark;
                else if (choice == 5 && square[5] == '5')square[5] = mark;
                else if (choice == 6 && square[6] == '6')square[6] = mark;
                else if (choice == 7 && square[7] == '7')square[7] = mark;
		        else if (choice == 8 && square[8] == '8')square[8] = mark;
                else if (choice == 9 && square[9] == '9')
			    square[9] = mark;
		     else{
			     cout<<"Invalid move ";
			     player--;
			     getch();}
		         i=checkwin();
		         player++;}
             while(i==-1);
                 board();
	             if(i==1)cout<<"==>\aPlayer "<<--player<<" win ";
	         else
                 cout<<"==>\aGame draw";
	             getch();
	             return 0;}

      int checkwin(){
	         if (square[1] == square[2] && square[2] == square[3])return 1;
             else if (square[4] == square[5] && square[5] == square[6])return 1;
	         else if (square[7] == square[8] && square[8] == square[9])return 1;
	         else if (square[1] == square[4] && square[4] == square[7])return 1;
	         else if (square[2] == square[5] && square[5] == square[8])return 1;
             else if (square[3] == square[6] && square[6] == square[9])return 1;
             else if (square[1] == square[5] && square[5] == square[9])return 1;
             else if (square[3] == square[5] && square[5] == square[7])return 1;
             else if (square[1] != '1' && square[2] != '2' && square[3] != '3' &&
	                  square[4] != '4' && square[5] != '5' && square[6] != '6' &&
                      square[7] != '7' && square[8] != '8' && square[9] != '9')return 0;
	         else
                return -1;}


     void board(){
            cout << "\n\n\tTic Tac Toe\n\n";
	        cout << "Player 1 (X)  -  Player 2 (O)" << endl << endl;
	        cout << endl;
            cout << "     |     |     " << endl;
            cout << "  " << square[1] << "  |  " << square[2] << "  |  " << square[3] << endl;
            cout << "_____|_____|_____" << endl;
	        cout << "     |     |     " << endl;
	        cout << "  " << square[4] << "  |  " << square[5] << "  |  " << square[6] << endl;
	        cout << "_____|_____|_____" << endl;
	        cout << "     |     |     " << endl;
            cout << "  " << square[7] << "  |  " << square[8] << "  |  " << square[9] << endl;
	        cout << "     |     |     " << endl << endl;}

};



int main()
{
    login_account obj;
    int choice;
    jump:
    cout<<"                                         "<<"********************************************"<<endl;
    cout<<"                                         "<<"********************************************"<<endl;
    cout<<"                                         "<<"******************                   *******"<<endl;
    cout<<"                                         "<<"*****************                    *******"<<endl;
    cout<<"                                         "<<"****************                     *******"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"**********     Mini Facebook   *************"<<endl;
    cout<<"                                         "<<"*(C)2018 ROHAN FAROOQUI ALL RIGHTS RESERVED*"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************     :)   ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"****************          ******************"<<endl;
    cout<<"                                         "<<"********************************************"<<endl;
    cout<<"                                         "<<"********************************************"<<endl;
    cout<<"                                                                                         "<<endl;
    cout<<"                                         "<<"*------------Plz Choose a Option-----------*"<<endl;
    cout<<"                                         "<<"|-> Press (1) To Login in Existing Account |"<<endl;
    cout<<"                                         "<<"|-> Press (2) To Create New Account        |"<<endl;
    cout<<"                                         "<<"|-> press (3) To Exit                      |"<<endl;
    cout<<"                                         "<<"*------------------------------------------*"<<endl;
    cout<<"                                         "<<"--------------------------------------------"<<endl;
    cout<<"                                         "<<"Select an Option : ";
    cin>>choice;
    if(choice == 1){
      obj.login_acc();}
    else if(choice == 2){
      obj.acc_info();
      goto jump;}
    else if(choice == 3){
      exit(0);}
    else{
        system("cls");
        goto jump;
    }




}

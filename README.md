#include <iostream>
#include <vector>
using namespace std;
struct List{
    string item;
}; List list;
vector <List> v1;
int main(){
    while(true){
        int choice;
        cout << "1. For add items "<<endl; 
        cout << "2. For searching the item"<<endl; 
        cout << "3. For exit"<<endl; 
        cout<< "Enter your choice: "; cin>>choice;
        if (choice==1){
            system("cls");
            int total;
            cout<<"How many items do you want to add! ";
            cin >> total;
            for (int i=0; i<total; i++){
                cout<<"Name : ";  cin>>list.item;
                v1.push_back(list);
                cout<<"Saved item: "<<i+1<<endl;
            }
        }
        else if (choice==2){
            system("cls");
            string s;
            cout<<"Enter the name of the item you want to serach : "; cin>>s;
            for (int i=0; i<v1.size(); i++){
                if (s==v1[i].item){
                    system("cls");
                    cout<<"Match found :"<<endl<<endl;
                }
                else {
                    system("cls");
                    cout<< "Match not found :"<<endl<<endl;
                }
            }
        }
        else if (choice==3){
            exit(0);
        }
        else{
            cout<<"Invaild Choice...."<<endl<<endl;
        }
    }
    return 0;
}

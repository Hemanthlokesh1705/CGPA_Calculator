#include<iostream>
using namespace std;
long total_credit=0;
float percentage=0;
class four{
   const int f[7]={40,36,32,28,24,20,16};
    public:
    int calculate(int x){
        if(x>=90){
            return f[0];
        }
        else if(x>=80&&x<90){
            return f[1];
        }
        else if(x>=70&&x<80){
            return f[2];
        }
        else if(x>=60&&x<70){
            return f[3];
        }
        else if(x>=50&&x<60){
            return f[4];
        }
        else if(x>=40&&x<50){
            return f[5];
        }
        else {
            cout<<"F"<<endl;
            return 0;
        }
    }
};
class three{
   const int t[7]={30,27,24,21,18,15,12};
    public:
    int calculate_three(int y){
    if(y>=90){
            return t[0];
        }
        else if(y>=80&&y<90){
            return t[1];
        }
        else if(y>=70&&y<80){
            return t[2];
        }
        else if(y>=60&&y<70){
            return t[3];
        }
        else if(y>=50&&y<60){
            return t[4];
        }
        else if(y>=40&&y<50){
            return t[5];
        }
        else {
            cout<<"F"<<endl;
            return 0;
        }
    }

};
class one{
   const int o[7]={10,9,8,7,6,5,4};
    public:
    int calculate_one(int z){
          if(z>=90){
            return o[0];
        }
        else if(z>=80&&z<90){
            return o[1];
        }
        else if(z>=70&&z<80){
            return o[2];
        }
        else if(z>=60&&z<70){
            return o[3];
        }
        else if(z>=50&&z<60){
            return o[4];
        }
        else if(z>=40&&z<50){
            return o[5];
        }
        else {
            cout<<"F"<<endl;
            return 0;
        }

    }
};
int main(){
    cout<<endl;
    cout<<"Please enter your marks below between(0 to 100)"<<endl;
    cout<<endl;
    four f;
    int four_mark;
    for (int i=1;i<3;i++){
        cout<<"Enter the "<<i<<"st four credit marks : ";
        cin>>four_mark;
        percentage+=four_mark;
        total_credit+=f.calculate(four_mark);

    }
    three t;
    int three_mark;
    for (int i=1;i<4;i++){
        cout<<"Enter the "<<i<<"st three credit marks : ";
        cin>>three_mark;
        percentage+=three_mark;
        total_credit+=t.calculate_three(three_mark);

    }
    one o;
    int one_marks;
    for (int i=1;i<4;i++){
        cout<<"Enter the "<<i<<"st one credit marks : ";
        cin>>one_marks;
         percentage+=one_marks;
        total_credit+=o.calculate_one(one_marks);

    }
    cout<<endl;
    cout<<"--------------DISPLAY OF SCORECARD-------------"<<endl;
    cout<<endl;
    cout<<"Total_credits obtained : "<<total_credit<<endl;
    float sgpa=(float(total_credit)/200)*10;
    cout<<"Your SGPA is : "<<sgpa<<endl;
    float total_percentage=(percentage/800)*100;
    cout<<"Your Percentage is :"<<total_percentage<<"%"<<endl;
    cout<<endl;

    cout<<"Are you 2nd sem student?"<<endl;
    cout<<"Type yes if you are else no : ";
    float two_sgpa;
    
    
    string opinion;
    cin>>opinion;
    float cgpa;
    if(opinion =="yes"){
        cout<<"Please enter your last semester SGPA : ";
        cin>>two_sgpa;
        cgpa=(two_sgpa+sgpa)/2;
        cout<<"Your cgpa is : "<<cgpa<<endl;
        cout<<endl;

    }
    else{
        cout<<endl;
        cout<<"---THANK YOU---"<<endl;
        cout<<endl;
    }

    return 0;
}

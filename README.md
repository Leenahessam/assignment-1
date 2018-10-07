# assignment-1
/this program turn time from the 12 hours format into 24
//turns time into four-digit military time
#include <iostream>
#include <string>
using namespace std;
float hour,minute;
string x;
void time (int h,int m,string y){
if (y=="am"){
    if (h==12){
        h=00;
       if (m/10.0<1){
            cout<<0<<h<<0<<m<<" hours"<<endl;
        }
        else if (m/10.0>1 || m/10.0==1){
            cout<<0<<h<<m<<" hours"<<endl;
        }
    }
    else if (h/10.0<1){
        if (m/10.0<1){
            cout<<0<<h<<0<<m<<" hours"<<endl;
        }
        else if (m/10.0>1 || m/10.0==1){
            cout<<0<<h<<m<<" hours"<<endl;
        }
    }
    else if (h/10.0>1){
        if (m/10.0<1){
            cout<<h<<0<<m<<" hours"<<endl;
        }
        else if (m/10.0>1 || m/10.0==1){
            cout<<h<<m<<" hours"<<endl;
        }
    }
}
else if (y=="pm"){
    if (h==12){
        if (m/10.0<1){
            cout<<h<<0<<m<<" hours"<<endl;
        }
        if (m/10.0>1 || m/10.0==1){
            cout<<h<<m<<" hours"<<endl;
        }
    }
    else {
        h=h+12;
        if (m/10.0<1){
            cout<<h<<0<<m<<" hours"<<endl;
        }
        if (m/10.0>1 || m/10.0==1){
            cout<<h<<m<<" hours"<<endl;
        }
    }
}
}

int main()
{
    cout << " please, enter time in HH:MM AM/PM format \n enter hour   : ";
    cin>>hour;
    cout<<" enter minutes: ";
    cin>>minute;
    cout<<" AM/PM        : ";
    cin>>x;
    time(hour,minute,x);

    return 0;
}

#include <iostream>
#include<string>
using namespace std;

class Student
{
    protected:
    int id;
    string name;
    public:
    void getstd()
    {
        cout<<"Enter student id:";
        cin>>id;
        cout<<"enter student name:";
        cin>>name;
    }
    void putstd()
    {
        cout<<"student name is:"<<name<<endl;
        cout<<"student id:"<<id<<endl;
    }
};
class Marks:public Student
{
    protected:
    float p,c,m;
    public:
    void getmarks()
    {
        cout<<"Enter physics,chemistry & maths marks:"<<endl;
        cin>>p>>c>>m;
    }
    void putmarks()
    {
            cout<<"physics marks:"<<p<<endl;
            cout<<"Chemsitry marks:"<<c<<endl;
            cout<<"Maths marks:"<<m<<endl;
    }
    
};
class Spmarks
{
  protected:
  float s;
  public:
  void getSpmark()
  {
      cout<<"enter sports marks:"<<endl;
      cin>>s;
     
  }
  void putSpmark()
  {
      cout<<"sports marks:"<<s<<endl;
  }
};
class Result:public Marks,public Spmarks
{
    
    float total,avg;
    public:
    void show()
    {
        total=p+c+m+s;
        avg=p+c+m+s/4;
        cout<<"total marks of student is:"<<total<<endl;
         cout<<"average marks of student is:"<<avg<<endl;
    }
    
};
int main()
{
   Result R;
   R.getstd();
   R.putstd();
   R.getmarks();
   R.putmarks();
   R.getSpmark();
   R.putSpmark();
   R.show();
}

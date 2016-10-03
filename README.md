# Inheritance-
#include <iostream>
#include <cstdlib>

using namespace std;

class UZ_Student{
    string regNum;
    string name;
    int age;

    public:
        void student(){
        cout << "Name: Nigel Mawoko \nRegistration Number: R156441Y \nStudent Age: 20\n " << endl;
        }
    };

class SOT: public UZ_Student{
    int Intake;

    public:
        void yourIntake(){
        cout << "Intake: 17\n" << endl;
        }
    };

class Med: public UZ_Student{
    int Semester;

    public:

    };

class DAIT: public SOT{
    string BestSubject;
    string WorstSubject;

    public:
        void YourSubjects(){
        cout << "Student's best subject: Math \n" << endl;
        cout << "Student's worst subject: Accounting \n" << endl;
        }
    };

class CAIT: public SOT{


    };

class Software: public DAIT{
    string coreCourse;

    public:
        void yourCoreCourse(){
        cout << "Student's core course: Software \n" << endl;}
    };

class Hardware: public DAIT{
    string CoreCourse;

    public:
        void your_coreCourse();

    };

class All: public Software{
    string displayInfo;

    public:
        void displayInformation(){
        cout << " Thank You \n" << endl;
        }
    };

int main()
{
    All everything;
    Hardware hardware_display;

    everything.student();
    everything.yourCoreCourse();
    hardware_display.yourIntake();
    hardware_display.YourSubjects();
    everything.displayInformation();

    return 0;
}

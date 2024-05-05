# GPA-Calculator

#include <iostream>
#include <string>

using namespace std;
int main()
{
    float N, marks, hours, points, totalP = 0, totalH = 0, GPA;
    string course;

    cout << "Welcome to a GPA Calculator App" << endl;
    cout << "Please Enter the number of Registered Courses : ";
    cin >> N;

    for ( int i = 0; i < N; i++)
    {
        cout << "Please Enter Course Name " << "#" << i+1 << ": ";
        cin >> course;

        cout << "Please Enter the mark of Course " << course << ": ";
        cin >> marks;

        if ( marks <= 100 && marks >= 95)
        {
            points = hours * 5.00;
        } else if ( marks < 95 && marks >= 90)
        {
            points = hours * 4.75;
        } else if ( marks < 90 && marks >= 85)
        {
            points = hours * 4.50;
        } else if ( marks < 85 && marks >= 80)
        {
            points = hours * 4.00;
        } else if ( marks < 80 && marks >= 75)
        {
            points = hours * 3.50;
        } else if ( marks < 75 && marks >= 70)
        {
            points = hours * 3.00;
        } else if ( marks < 70 && marks >= 65)
        {
            points = hours * 2.50;
        } else if ( marks < 65 && marks > 60)
        {
            points = hours * 2.0;
        } else 
        {
            cout << "Please Enter correct Mark: " << endl;
            return marks;
        }
        totalP += points;
        totalH += hours;
    }
    GPA = totalP / totalH;
    cout << "Your GPA is : " << GPA << endl;
    return 0;
}

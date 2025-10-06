1."WATERMALON (4A)"

#include <iostream>
using namespace std;

int main (){
    int w;
    cin>>w;

    if (w>=1 && w<=100 && w%2==0 && w>2)
    {
        cout<<"YES"<<endl;
    }
    else
    {
        cout<<"NO"<<endl;
    }

    return 0;
}

2."TEAM (231 A)"

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int counts = 0;

    for (int i = 0; i < n; i++)
    {

        int a, b, c;

        cin >> a >> b >> c;

        int sum = a + b + c;

        if (sum >= 2)
        {
            counts++;
        }
    }

    cout << counts << endl;
    return 0;
}

3.B++ (282A)

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    int x = 0;
    string s;

    for (int i = 0; i < n; i++) {
        cin >> s;  // read statement

        if (s == "++X" || s == "X++")
            x++;
        else if (s == "--X" || s == "X--")
            x--;
    }

    cout << x << endl;
    return 0;
}




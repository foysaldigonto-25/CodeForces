1.WATERMALON (4A)

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

2.TEAM (231 A)

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

4.Domino piling 50A

#include <iostream>
using namespace std;

int main (){

   int m,n;
   
   cin>>m>>n;
   
   int area = m*n;
   
   int totalDomino = area/2;
   cout <<totalDomino<<endl;

   
   return 0;
   
}


5.Helpful maths (339A)

#include <iostream>
#include <algorithm>
#include <string>
using namespace std;

int main() {
    string s;
    cin >> s;

    string num = "";
    for (char c : s)
        if (c != '+') num += c;

    sort(num.begin(), num.end());

    for (int i = 0; i < num.size(); i++) {
        cout << num[i];
        if (i < num.size() - 1) cout << "+";
    }

    return 0;
}

6.Bear and Big Brother (791 A)

#include <iostream>
using namespace std;

int main() {
    int a, b;
    cin >> a >> b;

    int years = 0;
    while (a <= b) {
        a = a * 3;
        b = b * 2;
        years++;
    }

    cout << years << endl;
    return 0;
}

7.Elephant (617A)

#include <iostream>
using namespace std;

int main() {
    int x;
    cin >> x;

    int steps;
    if (x % 5 == 0)
        steps = x / 5;
    else
        steps = (x / 5) + 1;

    cout << steps << endl;
    return 0;
}

8.Soldier and Bananas (546A)

#include <iostream>
using namespace std;

int main() {
    int k, n, w;
    cin >> k >> n >> w;

    int total = k * w * (w + 1) / 2;

    if (total > n)
        cout << total - n;
    else
        cout << 0;

    return 0;
}

9.Anton and Danik (734A)

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    string s;
    cin >> s;

    int anton = 0, danik = 0;

    for (char c : s) {
        if (c == 'A') anton++;
        else if (c == 'D') danik++;
    }

    if (anton > danik) cout << "Anton";
    else if (danik > anton) cout << "Danik";
    else cout << "Friendship";

    return 0;
}

10.In Search of an Easy Problem (1030A)

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;         
    int opinion;
    bool hard = false; 

    for (int i = 0; i < n; i++) {
        cin >> opinion;
        if (opinion == 1) {  
            hard = true;
        }
    }

    if (hard)
        cout << "HARD";
    else
        cout << "EASY";

    return 0;
}

11.	George and Accommodation (467A)

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n; // number of rooms

    int count = 0; 
    for (int i = 0; i < n; i++) {
        int p, q;
        cin >> p >> q; 
        if (q - p >= 2) { 
            count++;
        }
    }

    cout << count << endl; 
    return 0;
}

11.Wrong Subtraction (977A)

#include <iostream>
using namespace std;

int main() {
    long long n;
    int k;
    cin >> n >> k;

    for (int i = 0; i < k; i++) {
        if (n % 10 == 0)
            n /= 10;
        else
            n -= 1;
    }

    cout << n << endl;
    return 0;
}

12.344A	Magnets

#include <iostream>
#include <string>
using namespace std;

int main() {
    int n;
    cin >> n;
    string magnet;
    cin >> magnet;  

    int groups = 1; 
    string prev = magnet;

    for (int i = 1; i < n; i++) {
        cin >> magnet;
        if (magnet != prev) {
            groups++;
        }
        prev = magnet;
    }

    cout << groups << endl;
    return 0;
}

13.(200B) Drinks

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    double sum = 0.0;
    for (int i = 0; i < n; i++) {
        double p;
        cin >> p;
        sum += p;
    }
    cout << sum / n << endl;
    return 0;
}

14.(61A) Ultra-Fast Mathematician

#include <iostream>
#include <string>
using namespace std;

int main() {
    string a, b;
    cin >> a >> b;

    for (int i = 0; i < a.size(); i++) {
        if (a[i] == b[i])
            cout << '0';
        else
            cout << '1';
    }
    cout << endl;
    return 0;
}

15.(144A) Arrival of the General

#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int i = 0; i < n; i++) cin >> a[i];

    int maxPos = 0, minPos = 0;

    for (int i = 0; i < n; i++) {
        if (a[i] > a[maxPos]) maxPos = i;    
        if (a[i] <= a[minPos]) minPos = i;    
    }

    int ans = maxPos + (n - 1 - minPos);
    if (maxPos > minPos) ans--;   

    cout << ans << endl;
    return 0;
}

16.(1328A) Divisibility Problem

#include <iostream>
using namespace std;

int main() {
    int t;
    cin >> t;
    while (t--) {
        long long a, b;
        cin >> a >> b;
        if (a % b == 0)
            cout << 0 << endl;
        else
            cout << b - (a % b) << endl;
    }
    return 0;
}

17.(996A) Hit the Lottery

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    int bills[] = {100, 20, 10, 5, 1};
    int count = 0;
    for (int i = 0; i < 5; i++) {
        count += n / bills[i];
        n %= bills[i];
    }
    cout << count;
    return 0;
    }

18.(151A) Soft Drinking

#include <bits/stdc++.h>
using namespace std;

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    
    int n, k, l, c, d, p, nl, np;
    cin >> n >> k >> l >> c >> d >> p >> nl >> np;
    
    int drink = (k * l) / nl;
    int lime = c * d;
    int salt = p / np;
    
    int toasts = min({drink, lime, salt}) / n;
    
    cout << toasts << '\n';
    return 0;
}

















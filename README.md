# C++ online compiler
1. [programiz](https://www.programiz.com/cpp-programming/online-compiler/)
2. [onlinegdb](https://www.onlinegdb.com/online_c++_compiler)
3. [cpp](https://cpp.sh/)
4. [tutorialspoint](https://www.tutorialspoint.com/compile_cpp_online.php)
---

# input 
[\#include \<iostream\>](https://www.programiz.com/cpp-programming/library-function/cstdio/scanf)  
```
scanf("%d%c%s%lf%f", &a,&b,&c,&d,&e);  
```

[\#include \<string\>](https://cplusplus.com/reference/string/string/getline/)  
```
string input;  
getline(cin, input);
```

# printf  
[\#include \<cstdio\>](https://www.programiz.com/cpp-programming/library-function/cstdio/printf#google_vignette)  

``` 
printf("%.0f", 2 * c);  
printf("%.9lf", a/b);
```

# sort
[\#include \<algorithm\>](https://modoocode.com/272)
```
reverse(nums.begin(), nums.end());
sort(nums.begin(), nums.end());
```


# 대소문자  
[ASCii](https://namu.wiki/w/%EC%95%84%EC%8A%A4%ED%82%A4%20%EC%BD%94%EB%93%9C)  
[\#include \<cctype\>](https://www.programiz.com/cpp-programming/library-function/cctype/tolower)  
``` 
isupper(ch)  
tolower(ch)

'A' + 32 --> 'a'
'a' - 32 --> 'A'
```
[\#include \<algorithm\>](https://cplusplus.com/reference/algorithm/transform/)
```
for(auto& ch : strArr){
        if (idx & 1) transform(ch.begin(), ch.end(), ch.begin(), ::toupper);
        else transform(ch.begin(), ch.end(), ch.begin(), ::tolower);
```

# 3항 연산자
```
ch == alp[0] ? ch -= 32 : ch;

n % 2 ? printf("%d is odd", n) : printf("%d is even", n);

for(auto& i : arr)
        i = (i & 1) ? (i < 50 ? i << 1 : i) : (i >= 50 ? i >> 1 : i);

i & 1 ? i << 1  : i >> 1 ;
// odd number ? i * 2^1 : i / 2^1
```

# 슬라이싱
[\#include \<vector\>](https://www.programiz.com/cpp-programming/vectors)
```
vector(nums.begin(), nums.begin() +n);
vector(nums.begin() + n - 1, nums.end());
```

[\#include \<string\>](https://cplusplus.com/reference/string/string/assign/)
```
str.substr(0, n);

answer.assign(str.begin(), str.begin()+n);

return string(str.begin(), str.begin()+n);
```

# type 변환
[\#include \<cmath\>](https://www.programiz.com/cpp-programming/library-function/cmath/floor)  
[\#include \<string\>](https://www.programiz.com/cpp-programming/string-int-conversion)
```
stoi("25")  --> 25
stoi('1')   --> ERROR
'9' - '0'   --> 9
'10' - '0'  --> 12544
'5' - 48    --> 5
```
```
double flo;
floor(flo);

int a=10, b=10;
max(stoi(to_string(a)), 2 *b);
```
# type 확인
[\#include \<typeinfo\>](https://www.ibm.com/docs/ko/i/7.5?topic=expressions-typeid-operator-c-only)
```
int a = 10;
cout <<  typeid(a).name();
```

# find
[\#include \<string\>](https://modoocode.com/241)
```
string str1 = "abc", str2 = "aabcc";
    // cout << str2.find(str1); // str1이 존재하면 str2에 시작점의 idx가 output으로 아니라면 18446744073709551615
    // cout << string::npos; // 18446744073709551615
    // the greatest possible value
return str2.find(str1) != string::npos ? 1 : 0;
```
[\#include \<algorithm\>](https://modoocode.com/261)
```
#include <vector>
if (find(arr.begin(), arr.end(), num) != arr.end()) // 값이 존재한다.
            {// idx 알려줘.
            idx = find(arr.begin(), arr.end(), num) - arr.begin();
            // 해당 idx의 값을 삭제해줘.
            arr.erase(arr.begin() + idx);
```

# replace
[\#include \<string\>](https://modoocode.com/250)
```
str.replace(i, 1, "rn");
//str[i] 위치에서 길이 1 만큼의 단어를 rn으로 바꿔줘.
```
[\#include \<regex\>](https://modoocode.com/303)
```
regex_replace(str, regex("m"),"rn"); 
// m 이란 문자를 rn으로 바꿔줘.
```

# remove
[\#include \<algorithm\>](https://modoocode.com/266)  
[\#incldue \<cctype\](https://www.programiz.com/cpp-programming/library-function/cctype/isspace)
```
#include <iostream>
#include <string>
using namespace std;
//algorithm --> remove_if
//cctype --> isspace
string input;
getline(cin, input);
input.erase(remove_if(input.begin(), input.end(), ::isspace), input.end());
printf("%s", input.c_str());
```
> apple pen -> applepen

# 그 외
```
!(false) == true;
```

[\#include \<set\>](https://www.geeksforgeeks.org/set-in-cpp-stl/)
[\#include \<cmath\>](https://www.geeksforgeeks.org/python-cmath-sqrt-method/?ref=header_search)
```
set<int> s{a, b, c};
pow(a,3);
```


[\#include \<limits\>](https://cplusplus.com/reference/limits/numeric_limits/)
```
numeric_limits<int>::max();
```

[\#include \<string\>](https://cplusplus.com/reference/string/string/npos/)
```
cout << std::string::npos;
//the greatest possible value -> 18446744073709551615
// "until the end of the string".
```
[\#include \<numeric\>](https://cplusplus.com/reference/numeric/accumulate/)
```
num_list.size() <= 10 ?
//answer = 1에서 1개씩 곱하는 것.
    accumulate(nums.begin(), nums.end(), 1, multiplies<int>()) :
//answer = 0 에서 한개씩 더하는 것
    accumulate(nums.begin(), nums.end(), 0);


accumulate(arr.begin(), arr.end(), string());
```
> ['a','b','c'] --> "abc"

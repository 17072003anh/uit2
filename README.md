# uit2
#include <iostream>
using namespace std;
#define MAXN 100
struct stack{
	int s[MAXN];
	int n;
};
bool empty(const stack &s){
	return s.n == 0;
}
bool full(const stack &s){
	return s.n == MAXN;
}
int top(const stack &s){
	return s.s[s.n-1];
}
void pop(stack &s){
	s.s[s.n--] = 0;
}
void push(stack &s, const int &x){
	s.s[s.n++]=x;
}

void Testing_Push_Pop_Top_Stack(stack &s){
	int x;
	cin >> x;
	cout << "output: ";
	while (x!=-1){
		if(x!=0) push(s, x);
		else {
		if (empty(s) != true){
		 cout << top(s) <<" ";
		pop(s); 
			}
		}
	cin >> x;
	}
	cout << "\ntop: ";
	if(!empty(s)) cout << top(s); 
}
int main() {
    stack s;
    Testing_Push_Pop_Top_Stack(s);
    return 0;
}

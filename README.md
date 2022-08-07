# DCIT-104-assignment-prime-numbers-
// 10953537 is my Student ID
// this is a c++ code that check and calculate the sume of prime numbers within a range 
#include <iostream>
using namespace std;

bool checkPrime(int numberToCheck)
{
	if(numberToCheck == 1) {
		return false;
	}
	for (int i = 2; i*i <= numberToCheck; i++) {
		if (numberToCheck % i == 0) {
			return false;
		}
	}
	return true;
}


int primeSum(int l, int r)
{
	int sum = 0;
	for (int i = r; i >= l; i--) {

		bool isPrime = checkPrime(i);
		if (isPrime) {

			sum = sum + i;
		}
	}
	return sum;
}

int main()
{
	int l = 4, r = 13;
	cout << primeSum(l, r);
}

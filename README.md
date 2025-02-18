#include <iostream>
#include <bitset>
#include <cmath>
using namespace std;

double sqrtBinary(int number) {
    return sqrt(number);
}
string toBinary(int number) {
    return bitset<32>(number).to_string();
}
int main() {
    int number;
    cout << "Введите число: ";
    cin >> number;
    
    if (number < 0) {
        cout << "Ошибка: квадратный корень из отрицательного числа не определен." << endl;
        return 1;
    } 
    int sqrtResult = static_cast<int>(sqrtBinary(number));
    string binaryResult = toBinary(sqrtResult);
    binaryResult = binaryResult.substr(binaryResult.find('1'));
    cout << "Квадратный корень: " << sqrtResult << endl;
    cout << "В двоичной системе: " << binaryResult << endl;
    return 0;
}

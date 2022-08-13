# Rock-Paper-Scissor
Simple C++ code that allows the user to play rock-paper-scissor with the computer

```
#include <iostream>

using namespace std;

int main() {
    int player2, r2d2, counter, r2d2Point = 0, player2Point = 0;
    cout << "1: rock" << endl << "2: paper" << endl << "3: scissor" << endl;
    counter = 5;
    while (counter > 0) {
        cout << "Pick your move: ";
        cin >> player2;
        srand(time(0));
        r2d2 = rand()%2 + 1;
        if (player2 == 1) {
            cout << "You choose rock" << endl;
            if (r2d2 == 1) {
                cout << "Both players chose the same move. This round does not count" << endl;
                continue;
            }
            else if (r2d2 == 2) {
                cout << "R2D2 wins!" << endl;
                r2d2Point++;
            }
            else if (r2d2 == 3) {
                cout << "You win!" << endl;
                player2Point++;
            }
        }
        if (player2 == 2) {
            cout << "You chose paper" << endl;
            if (r2d2 == 1) {
                cout << "You wins!" << endl;
                player2Point++;
            }
            else if (r2d2 == 2) {
                cout << "Both players chose the same move. This round does not count" << endl;
                continue;
            }
            else if (r2d2 == 3) {
                cout << "R2D2 wins!" << endl;
                r2d2Point++;
            }
        }
        if (player2 == 3) {
            cout << "You chose scissor" << endl;
            if (r2d2 == 1) {
                cout << "R2D2 wins!" << endl;
                r2d2Point++;
            }
            else if (r2d2 == 2) {
                cout << "You wins!" << endl;
                player2Point++;
            }
            else if (r2d2 == 3) {
                cout << "Both players chose the same move. This round does not count" << endl;
                continue;
            }
        }
        if (player2Point == 3) {
            cout << endl << "You win the game!";
            break;
        }
        else if (r2d2Point == 3) {
        cout << endl << "You lose the game!";
        break;
        }
        counter--;
    }
    if (player2Point != 3 and r2d2Point != 3)
    cout << endl << "nobody won the game";
    return 0;
}

```

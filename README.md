//Zip-Password-Cracker//
#include <iostream>
#include <ctime>
using namespace std;
string crackPassword(string pass);
long long int attempt;
clock_t start_t, end_t;

int main(){
    string password;

    cout << "Enter the password to crack(max 5 digit): ";
    cin >> password;
	
	cout << "\n\nPlease wait...\n";
    cout << endl << endl << endl << ">\n>> CRACKED THE PASSWORD! >>\n>" << endl <<  endl <<"The password : " << crackPassword(password) << endl;
    cout << "Total number of attempts : " << attempt << endl;
    cout << "Total time duration passed : " << (double)(end_t - start_t)/1000 << " sec" << endl << endl;
    return 0;
}

string crackPassword(string pass){
    int digit[7],alphabetSet=1,passwordLength=1;
    start_t = clock();

    string test,alphabet = " ";
    while(1){


            switch(passwordLength){
                case 1:
                    while(alphabetSet<4){
                    switch(alphabetSet){
                        case 1 : alphabet = "0123456789";
                                 break;
                        case 2 : alphabet = "abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 3 : alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        }

                    for(digit[0]=1;digit[0]<alphabet.length();digit[0]++){
                                                    attempt++;
                                                    test=alphabet[digit[0]];
                                                    for(int i=1;i<passwordLength;i++)
                                                        if(alphabet[digit[i]]!=' ')test+=alphabet[digit[i]];
                                                    if(pass.compare(test)==0){end_t=clock(); return test;}
                                                    }
                                                    alphabetSet++;
                    }
                    break;
                case 2:
                    alphabetSet=1;
                    while(alphabetSet<6){
                    switch(alphabetSet){
                        case 1 : alphabet = "0123456789";
                                 break;
                        case 2 : alphabet = "abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 3 : alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 4 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 5 : alphabet = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                        }
													{
                                                    attempt++;
                                                    test=alphabet[digit[0]];
                                                    for(int i=1;i<passwordLength;i++)
                                                        if(alphabet[digit[i]]!=' ')test+=alphabet[digit[i]];
                                                    if(pass.compare(test)==0){end_t=clock(); return test;}
                                                    }
                                                    alphabetSet++;
                    }
                    break;
                case 3:
                    alphabetSet=1;
                    while(alphabetSet<8){
                    switch(alphabetSet){
                        case 1 : alphabet = "0123456789";
                                 break;
                        case 2 : alphabet = "abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 3 : alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 4 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 5 : alphabet = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 6 : alphabet = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 7 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                    }
                                        for(digit[2]=0;digit[2]<alphabet.length();digit[2]++)
                                            for(digit[1]=0;digit[1]<alphabet.length();digit[1]++)
                                                for(digit[0]=1;digit[0]<alphabet.length();digit[0]++){
                                                    attempt++;
                                                    test=alphabet[digit[0]];
                                                    for(int i=1;i<passwordLength;i++)
                                                        if(alphabet[digit[i]]!='-')test+=alphabet[digit[i]];
                                                    if(pass.compare(test)==0){end_t = clock(); return test;}
                                                    }
                                                    alphabetSet++;
                    }
                    break;
                case 4:
                    alphabetSet=1;
                    while(alphabetSet<8){
                    switch(alphabetSet){
                        case 1 : alphabet = "0123456789";
                                 break;
                        case 2 : alphabet = "abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 3 : alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 4 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 5 : alphabet = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 6 : alphabet = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 7 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                    }

                                    for(digit[3]=0;digit[3]<alphabet.length();digit[3]++)
                                        for(digit[2]=0;digit[2]<alphabet.length();digit[2]++)
                                            for(digit[1]=0;digit[1]<alphabet.length();digit[1]++)
                                                for(digit[0]=1;digit[0]<alphabet.length();digit[0]++){
                                                    attempt++;
                                                    test=alphabet[digit[0]];
                                                    for(int i=1;i<passwordLength;i++)
                                                        if(alphabet[digit[i]]!='-')test+=alphabet[digit[i]];
                                                    if(pass.compare(test)==0){end_t = clock(); return test;}
                                                    }
                                                    alphabetSet++;
                    }
                    break;
                case 5:
                    alphabetSet=1;
                    while(alphabetSet<8){
                    switch(alphabetSet){
                        case 1 : alphabet = "0123456789";
                                 break;
                        case 2 : alphabet = "abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 3 : alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 4 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyz";
                                 break;
                        case 5 : alphabet = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 6 : alphabet = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                        case 7 : alphabet = "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
                                 break;
                    }
                                for(digit[4]=0;digit[4]<alphabet.length();digit[4]++)
                                    for(digit[3]=0;digit[3]<alphabet.length();digit[3]++)
                                        for(digit[2]=0;digit[2]<alphabet.length();digit[2]++)
                                            for(digit[1]=0;digit[1]<alphabet.length();digit[1]++)
                                                for(digit[0]=1;digit[0]<alphabet.length();digit[0]++){
                                                    attempt++;
                                                    test=alphabet[digit[0]];
                                                    for(int i=1;i<passwordLength;i++)
                                                        if(alphabet[digit[i]]!='-')test+=alphabet[digit[i]];
                                                    if(pass.compare(test)==0){end_t = clock(); return test;}
                                                    }
                                                    alphabetSet++;
                    }
                    break;
            }
            passwordLength++;
    }
 }

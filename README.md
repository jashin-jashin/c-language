using namespace std; 
string S[5]= {"keyword","identifier","integer","boundary","operator"}; 
string T[6]= {"main","if","else","for","while","int"}; 
int main() {
string s;
while(cin>>s)
{
    int len=s.length();
    string temp="";
    for(int i=0; i<len; i++)
    {
        if(s[i] == '=' || s[i] == '+' || s[i] == '-'||s[i] == '*'|| s[i] == '/' || s[i] == '<' || s[i] == '>' || s[i] == '!')
        {
            if(temp.length())
            {
                panduan(temp);
            }
            temp="";
            if(i+1<len&&s[i+1]=='=')
            {
                cout<<"("<<S[4]<<","<<s[i]<<s[i+1]<<")"<<endl;
                i++;
            }
            else
            {
                cout<<"("<<S[4]<<","<<s[i]<<")"<<endl;
            }
        }
        else if(s[i] == '(' || s[i] == ')' || s[i] == '{'||s[i] == '}'|| s[i] == ',' || s[i] ==';')
        {
            if(temp.length())
            {
                panduan(temp);
            }
            temp="";
            cout<<"("<<S[3]<<","<<s[i]<<")"<<endl;
        }
        else
        {
            temp=temp+s[i];

        }
    }
    if(temp.length())
    {
        panduan(temp);
    }

}
return 0;}

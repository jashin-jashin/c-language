
void panduan(string s)
{
    if(s[0]>='0'&&s[0]<='9')
    {
        cout<<"("<<S[2]<<","<<s<<")"<<endl;
    }
    else
    {
        int f=1;
        for(int i=0; i<6; i++)
        {
            if(s==T[i])
            {
                f=0;
                cout<<"("<<S[0]<<","<<s<<")"<<endl;
                break;
            }
        }
        if(f==1)
        {
            cout<<"("<<S[1]<<","<<s<<")"<<endl;
        }
    }

}

# reverse-words-in-string
class Solution
{
    public:
    //Function to reverse words in a given string.
    string reverseWords(string S) 
    { 
        // code here 
    string ans="";
    string temp="";
    for(int i=S.size()-1;i>=0;i--){
        if(S[i]=='.')
        {
            reverse(temp.begin(),temp.end());
            ans+=temp;
            ans+='.';
            temp="";
        }
        else{
            temp+=S[i];
        }
    }
    reverse(temp.begin(),temp.end());
            ans+=temp;
            return ans;
    }
};

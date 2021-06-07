# frequency_of_char_in_the_strings

void printFreq(const string &board1 )
{
    unordered_map<string,int> wordFreq;
    stringstream ss1(board1);
    string word1;
    while (ss1>>word1)
    {
        wordFreq[word1]++;
    }
     
    unordered_map<string, int>:: iterator p;
   for (p = wordFreq.begin(); p != wordFreq.end(); p++)
   {
       cout<<"( "<<p->first<<" "<<p->second<<" )"<<endl;
   }
 
}
int main()
{
    string board="WWRRBBWW";
    string board1;
    for(int i = 0 ; i < board.length(); ++i) {
        board1 += board.substr(i, 1) + " ";
    }
    printFreq(board1);

    return 0;
}

using System;
using Microsoft.VisualBasic.FileIO;

namespace TRY
{
    class Program
    {
        void top()
        {
            String string1 = "Se învecinează cu România la vest și cu Ucraina la nord, est și sud.Republica Moldova este un stat fără ieșire directă la mare, " +
                             "însă are ieșire la Dunăre pe o fâșie de 430 de metri la extremitatea sa sudică,[14] prin intermediul căreia are acces potențial și la Marea Neagră." +
                             "În procesul dezmembrării Uniunii Sovietice, Republica Moldova și-a declarat independența la 27 august 1991. La 29 iulie 1994 a fost adoptată prima" +
                             "constituție a Republicii Moldova. Începând cu anul 1990, teritoriul Republicii Moldova situat pe malul estic al fluviului Nistru este sub control de" + 
                             "facto al regimului separatist din Transnistria (controlat și/sau sprijinit de Rusia).";  
            int count;  
          
            //Converts the string into lowercase  
            string1 = string1.ToLower();  
          
            //Split the string into words using built-in function  
            String[] words = string1.Split(' ');  
          
            Console.WriteLine("Duplicate words in a given string : ");  
            for(int i = 0; i < words.Length; i++) {  
                count = 1;  
                for(int j = i+1; j < words.Length; j++) {  
                    if(words[i].Equals(words[j])) {  
                        count++;  
                        //Set words[j] to 0 to avoid printing visited word  
                        words[j] = "0";  
                    }  
                }  
              
                //Displays the duplicate word if count is greater than 1  
                  if(count > 2 && words[i] != "0")  
                    Console.WriteLine(words[i]);  
            }  
        }
        static void Main(string[] args)
        {
            
            int i, wrd,l,p,wrd2;
            int len, vowel, cons, wrd3, len2;
	
            Console.Write("\n\nCount the total number of words in a string :\n");
            Console.Write("------------------------------------------------------\n");
            string str = "Republica Moldova este un stat situat în sud-estul Europei. Se învecinează cu România la vest și cu Ucraina la nord, est și sud. " +
                  "Republica Moldova este un stat fără ieșire directă la mare, însă are ieșire la Dunăre pe o fâșie de 430 de metri la extremitatea sa sudică, " +
                  "prin intermediul căreia are acces potențial și la Marea Neagră. În procesul dezmembrării Uniunii Sovietice, " +
                  "Republica Moldova și-a declarat independența la 27 august 1991. La 29 iulie 1994 a fost adoptată prima constituție a Republicii Moldova. " +
                  "Începând cu anul 1990, teritoriul Republicii Moldova situat pe malul estic al fluviului Nistru este sub control de facto al regimului separatist " +
                  "din Transnistria (controlat și/sau sprijinit de Rusia).";
            string[] words = str.Split(new[] { " " }, StringSplitOptions.None);
            l = 0;
            wrd = 1;
            wrd2 = 0;
            p = 0;

            /* loop till end of string */
            while (l <= str.Length - 1)
            {
                /* check whether the current character is white space or new line or tab character*/
                if(str[l]==' ' || str[l]=='\n' || str[l]=='\t')
                {
                    wrd++;
                }

                l++;
            }
            
            while (p <= str.Length - 1)
            {
                /* check whether the current character is white space or new line or tab character*/
                if(str[p]=='.' || str[p]=='\n' || str[p]=='\t')
                {
                    wrd2++;
                }

                p++;
            }
            
            vowel = 0;
            cons = 0;
            wrd3 = 0;
            len2 = str.Length;
            len = str.Length;

            for(i=0; i<len; i++)
            {

                if(str[i] =='a' || str[i]=='e' || str[i]=='i' || str[i]=='o' || str[i]=='u' || str[i]=='A' || str[i]=='E' || str[i]=='I' || str[i]=='O' || str[i]=='U')
                {
                    vowel++;
                }
                else if((str[i]>='a' && str[i]<='z') || (str[i]>='A' && str[i]<='Z'))
                {
                    cons++;
                }
            }
            
            for(i=0; i<len2; i++)
            {

                if(  str[i] =='A' || str[i]=='a' || str[i]=='B' || str[i]=='b' || str[i]=='C' || str[i]=='c' 
                   || str[i]=='E' || str[i]=='e' || str[i]=='F' || str[i]=='f' || str[i]=='G' || str[i]=='g' || str[i]=='H' || str[i]=='h' || str[i]=='I'
                   || str[i]=='i' || str[i]=='L' || str[i]=='l' || str[i]=='J' || str[i]=='j' || str[i]=='K' || str[i]=='k' || str[i]=='M' || str[i]=='m' 
                   || str[i]=='N' || str[i]=='n' || str[i]=='O' || str[i]=='o' || str[i]=='P' || str[i]=='p' || str[i]=='Q' || str[i]=='q' || str[i]=='R' 
                   || str[i]=='r' || str[i]=='S' || str[i]=='s' || str[i]=='T' || str[i]=='t' || str[i]=='U' || str[i]=='u' || str[i]=='V' || str[i]=='v' 
                   || str[i]=='Y' || str[i]=='y' || str[i]=='Z' || str[i]=='z') 
                {
                    wrd3++;
                }
            }
            
            string word = "";
            int ctr = 0;
            foreach (String s in words)
            {
                if (s.Length > ctr)
                {
                    word = s;
                    ctr = s.Length;
                }
            }
            
            Console.Write("Total number of words in the string is : {0}\n", wrd);
            Console.Write("Total number of sentences : {0}\n", wrd2);
            Console.Write("------------------------------------------------------\n");
            Console.Write("Total number of letters: {0}\n" ,wrd3);
            Console.Write("The total number of vowel in the string is : {0}\n", vowel);
            Console.Write("The total number of consonant in the string is : {0}\n", cons);
            Console.Write("------------------------------------------------------\n");
            Console.WriteLine("This is the longest word:  {0}" ,word);
        }
    }
}

----------------------------------------------------------------------------------------------------------------------------


static void Main() {
        String string1 = "Se învecinează cu România la vest și cu Ucraina la nord, est și sud.Republica Moldova este un stat fără ieșire directă la mare, " +
            "însă are ieșire la Dunăre pe o fâșie de 430 de metri la extremitatea sa sudică,[14] prin intermediul căreia are acces potențial și la Marea Neagră." +
            "În procesul dezmembrării Uniunii Sovietice, Republica Moldova și-a declarat independența la 27 august 1991. La 29 iulie 1994 a fost adoptată prima" +
            "constituție a Republicii Moldova. Începând cu anul 1990, teritoriul Republicii Moldova situat pe malul estic al fluviului Nistru este sub control de" + 
            "facto al regimului separatist din Transnistria (controlat și/sau sprijinit de Rusia).";  
        int count;  
          
        //Converts the string into lowercase  
        string1 = string1.ToLower();  
          
        //Split the string into words using built-in function  
        String[] words = string1.Split(' ');  
          
        Console.WriteLine("Duplicate words in a given string : ");  
        for(int i = 0; i < words.Length; i++) {  
            count = 1;  
            for(int j = i+1; j < words.Length; j++) {  
                if(words[i].Equals(words[j])) {  
                    count++;  
                    //Set words[j] to 0 to avoid printing visited word  
                    words[j] = "0";  
                }  
            }  
              
            //Displays the duplicate word if count is greater than 1  
            if(count > 2 && words[i] != "0")  
                Console.WriteLine(words[i]);
                
-------------------------------------------------------------------------------------

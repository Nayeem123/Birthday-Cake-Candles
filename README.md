# Birthday-Cake-Candles
You are in charge of the cake for your niece's birthday and have decided the cake will have one candle for each year of her total age. When she blows out the candles, she’ll only be able to blow out the tallest ones. Your task is to find out how many candles she can successfully blow out.  For example, if your niece is turning 4 years old, and the cake will have 4 candles of height  4,4 ,1 ,3 , she will be able to blow out 2 candles successfully, since the tallest candles  are of height 4 and there are 2 such candles.


Main Logic for this problem...
 // Complete the birthdayCakeCandles function below.
    static int birthdayCakeCandles(int[] ar) {
            Arrays.sort(ar);
            int c=1;
            int l=ar.length;
            if(l == 0)
            return 0;
            for(int i=l-1;i>0;i--)
            {
                if(ar[i] == ar[i-1])
                c++;
                else if(ar[i] != ar[i-1])
                break;
            }
        return c;
    }

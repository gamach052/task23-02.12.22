###  [Task 7 kyu](https://www.codewars.com/kata/554b4ac871d6813a03000035/train/java)

In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.


### My solution
```Java
public class Kata {
    public static String highAndLow(String numbers) {

        String[] splitStr = numbers.split(" ");
        int lNum = Integer.parseInt(splitStr[0]);
        int hNum = Integer.parseInt(splitStr[0]);
        for(int i=1; i<splitStr.length; i++){
            if(lNum>Integer.parseInt(splitStr[i]))
                lNum = Integer.parseInt(splitStr[i]);
            if(hNum<Integer.parseInt(splitStr[i]))
                hNum = Integer.parseInt(splitStr[i]);
        }


        return  String.valueOf(hNum)+" "+ String.valueOf(lNum);
    }
}


```

### Fav solution
```Java
import static java.util.Arrays.stream;

class Kata {
    static String highAndLow(String numbers) {
        var stats = stream(numbers.split(" ")).mapToInt(Integer::parseInt).summaryStatistics();
        return stats.getMax() + " " + stats.getMin();
    }
}
```
I like this solution because I like it

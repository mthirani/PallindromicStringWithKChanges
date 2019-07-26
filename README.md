# PallindromicStringWithKChanges

## Pseudo Code for the implemented algorithm:

Below is the main module which accepts the 'string' as the first argument and 'k' for maximum number of changes allowed and return the pallindromic string if formed within k changes else returns -1

```
function maximumPalinUsingKChanges(Argument string, Argument k){ 
  
    Step 1: Initialize l to 0 and r to the (string's length - 1) and create a palin array of characters from the input 'string'
    Step 2: If l is less than r then repeat steps 3 to 5
    Step 3: If each character in string at position l does not matches with the character in string at position r then take the maximum of that character 'digit' and put it in palin array at position l and r. Also decrement k by 1 then.
    Step 4: Increment l by 1
    Step 5: Decrement r by 1
    Step 6: If k is less than 0 then return "-1"
    Step 7: Initialize l to 0 and r to the (string's length - 1)
    Step 8: If l is less than or equal to r then repeat steps 9 to 13
    Step 9: If l equals r and k is > 0 then put '9' at position l in palin array
    Step 10: If character at position l in palin array is less than '9' and if none of the character at positions l and r is changed in the previous loop by checking (palin[l] = str.charAt(l) and palin[r] = str.charAt(r)) and k >= 2 then subtract 2 from k and convert both characters to 9 in palin array at respective positions l and r.
    Step 11: If character at position l in palin array is less than '9' and if one of the character at positions l and r is changed in the previous loop by checking (palin[l] != str.charAt(l) or palin[r] != str.charAt(r)) and k >= 1 then subtract 1 from k and convert both characters to 9 in palin array at respective positions l and r.
    Step 12: Increment l by 1
    Step 13: Decrement r by 1
  
    return the string formed from pallin array 
} 
```

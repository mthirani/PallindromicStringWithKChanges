# PallindromicStringWithKChanges

## Pseudo Code for the implemented algorithm:

Below is the main module which accepts the 'string' as the first argument, 'n' as String length and 'k' for maximum number of changes allowed and return the pallindromic string if formed within k changes else returns -1

```
function maximumPalinUsingKChanges(Argument string, Argument n, Argument k){ 
  
    Step 1: Initialize:: l = 0 and r = n - 1 and create a palin array of characters from the input 'string'
    Step 2: If l < r then repeat steps 3 to 5
    Step 3: If each character in string at position l does not matches with the character in string at position r by checking (str.charAt(l) != str.charAt(r)) then set palin[l] = palin[r] = max(str.charAt(l), str.charAt(r)) and set k = k - 1.
    Step 4: Increment l by 1
    Step 5: Decrement r by 1
    Step 6: If k < 0 then return "-1"
    Step 7: Initialize:: l = 0 and r = n - 1
    Step 8: If l <= r then repeat steps 9 to 13
    Step 9: If l = r and k > 0 then set palin[l] = '9'
    Step 10: If palin[l] < '9' and if none of the character at positions l and r is changed in the previous loop by checking (palin[l] = str.charAt(l) and palin[r] = str.charAt(r)) and k >= 2 then set k = k - 2 and set palin[l] = palin[r] = '9'.
    Step 11: If palin[l] < '9' and if one of the character at position l or r is changed in the previous loop by checking (palin[l] != str.charAt(l) or palin[r] != str.charAt(r)) and k >= 1 then set k = k - 1 and set palin[l] = palin[r] = '9'.
    Step 12: Increment l by 1
    Step 13: Decrement r by 1
  
    return the string formed from pallin array 
} 
```

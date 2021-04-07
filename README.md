# Replace-pi-recursive-

For understanding shift of characters, let's assume that the input string is “pipix” and assume that you have shifted some part of the input string and the input string is now: pi3.14x. Now, all you have to do is to replace the front part: pi3.14x. For this, you have to add 2 places to the input string first, so, we have to shift “3.14x” by 2 places and this will change the give string to pi_ _ 3.14x ( _ represents added 2 places of characters). Now, appropriate places can be replaced by 3.14 and hence, the string will become 3.143.14x.
Pseudocode:
if (input[0] == 'p' and input[1] == 'i')  // replacement should only be done if first 2 characters are 'p' and 'i'
    initialize count=0
    initialize i=0

    while(input[i]!='\0') //loop to count characters in string
        count++
        i++

    // shifting loop
    for (initialize i = count+1 condition: i >= 2 decrement: i--) 
            input[i + 2] = input[i]; //shifting

    //Replacement
    input[0] = '3'; 
    input[1] = '.'; 
    input[2] = '1'; 
    input[3] = '4'; 


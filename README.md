curl is used to retreive the page text
``` curl "url" ```
curl to return the page text and output to a file
``` curl "url" -O data.txt```

Process Text Data

1. Transform each space ' ' into a return character '\12' (aka ASCII line feed) THis basically converts each line to individual words
```tr ' ' '\12' < data.txt```
2. Pipe the output to sort (send the results of one command as input into another command) text will sort in ascending orders of alphabet
```tr ' ' '\12' < data.txt | sort ```
3. the sorted output to uniq -c to count. It gives the output how many times it has found each entry.
``` tr ' ' '\12' < data.txt | sort | uniq -c ```
4. reduced output to sort with -nr flag 
most duplicates to bubble up to the top
``` tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr ```
5. Redirect the output to result.txt 
the output will be redirected to the result.txt.
``` tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt ```
6. When we hit the up arrow in bash it will get the previous command we have used.
7. -n means numeric-value (it compares according to string numeric value)
8. -r means reverse (it reverse the result of comparisons sort according to WORD:)
9. Only one dash used for single letter flag 
10. Two dashes are used for long flags which are used for descriptive options.



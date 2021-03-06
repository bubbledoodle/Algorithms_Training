## Question
Given two strings s and t, determine if they are isomorphic.

Two strings are isomorphic if the characters in s can be replaced to get t.

All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character but a character may map to itself.

For example,
Given "egg", "add", return true.

Given "foo", "bar", return false.

Given "paper", "title", return true.

Note:
You may assume both s and t have the same length.

## Code
```JAVA
public class Solution {
    public boolean isIsomorphic(String s, String t) {
        int[] m1 = new int[256];
        int[] m2 = new int[256];
        int n = s.length();
        for (int i=0; i<n; i++){
            if(m1[s.charAt(i)] != m2[t.charAt(i)]) return false;
            m1[s.charAt(i)] = i+1;
            m2[t.charAt(i)] = i+1;
        }
        return true;
    }
}
```

## Thinking
想法是想到了的，代码实现上出了问题 anyway这些是可以借鉴的：
1. Utilizes the unicode. there is a unicode table maintained. Each entry tracks when did last time certain char appears.
2. Actually the table accessing is through char unicode indexing
3. 一直有个思维定式，construct then to compare, which theoretically consumes the same computational power. However, in real life the program can actually abandon the action while constructing if not match certain rules. 感觉这是行为哲学上的问题，试着改改呗。

And here's the table. It is a smart map that keeps all key a, b, c... __information as index accessing__ and the value as last time show up in string (index of string). 

| a | b | c |...| char| char|
|---|---|---|---|---|---|
| n1| n2| n3|...| n255| n256|

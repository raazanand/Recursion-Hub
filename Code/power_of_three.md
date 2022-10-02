---
Name: 'Raj Anand'
Github: 'https://github.com/raazanand'
WebSite: ''
Problem: 'Power of Three'
Description: 'Given an integer n, return true if it is a power of three. Otherwise, return false.'
Language: 'Java'
---



```java
public boolean isPowerOfThree(int n) {
        return helper((double) n);
    }
    private boolean helper(double n){
        if(n<1) return false;

        if(n==3 || n==1) {
            return true;
        }
        return helper(n/3);
    }
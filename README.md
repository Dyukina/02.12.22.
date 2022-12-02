# 02.12.22.

## 1. Create function fib that returns n'th element of Fibonacci sequence (classic programming task).

[Task link](https://www.codewars.com/kata/57a1d5ef7cb1f3db590002af/train/java)
___
### Мое рещение 
```java

public class Fibonacci { 
 public static long fib (int n) { 
 if (n <= 1) { 
 return n; 
 } 
  return fib(n - 1) + fib(n -2); 
 } 
}

```

### Понравившееся решение
```java

public class Fibonacci { 
 public static long fib(int n) { 
 long num1 = 0; 
 long num2 = 1; 
 System.out.println("N: " + n); 
 
  for (int i = 0; i < n - 1; i++) { 
 long temp = num1 + num2; 
 num1 = num2; 
 num2 = temp; 
 } 
 
  return num2; 
 } 
 
}

```
## 2. Count the number of divisors of a positive integer n. 
 
Random tests go up to n = 500000.
[Task link](https://www.codewars.com/kata/542c0f198e077084c0000c2e/train/java)
### Мое рещение 
```java

public class FindDivisor { 
 
 public long numberOfDivisors(int n) { 
 long counter = 0; 
 for(int i=1; i<=n; i++){ 
 if(n % i == 0){ 
 counter++; 
 } 
 } 
 return counter; 
 } 
}

```

### Понравившееся решение
```java

public class FindDivisor { 
 
 public long numberOfDivisors(int n) { 
 int cntr = 0; 
 for (int i = 1; i <= n/2; i++) 
 if (n % i == 0) cntr++; 
 return (n == 0)? 0 : ++cntr; 
 } 
 
}

```

# Converting Integers to Strings
There are a few different ways to convert Integers to Strings in java.

1. Using Integer.toString(int);
The argument is converted and returned as an instance of a String. If the number is negative the sign will be preserved.
```java 

int a = 1234;
String s1 = Integer.toString(a);

```

2. Using String.valueOf(int); 
```java
int c = 1234;
String s1 = String.valueOf(c);

```

3. Convert uing StringBuilder
```java
int f = 1234;
StringBuilder sb = new StringBuilder();
sb.append(g);
String s1 = sb.toString();
```

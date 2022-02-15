# Bitwise Logical Operators
 AND(&), OR(|), , and NOT(~)
 
# XOR(^) exclusive or、互斥或、異或
兩者一樣為false，兩者不一樣則為true，有以下幾個觀念:
* 交換率(Commutative property)，a ^ b = c => a ^ c = b, b ^ c = a
* 結合律(Associative property)，a ^ b ^ c = a ^ (b ^ c) = (a ^ b) ^ c
* x ^ x = 0
* x ^ 0 = x

```java
int i = 2; // 10
int j = 1; // 01
        
System.out.println(i^j); // 3,  11
```

# OR(|) 或
```java
int i = 2; // 10
int j = 1; // 01

System.out.println(i | j); //3,  11 
```
#  AND(&)
```java
int i = 5; // 101
int j = 3; // 011

System.out.println(i & j); //1, 001
```
# Bit Manipulation in Java
此章節主要介紹Java Bitwise operators。

## Java data type
* byte (8 bit)
* short (16 bit)
* int (32 bit)
* long (64 bit)
* char (16 bit)

# Bit Shift Operators

## Left shift
TODO

## Right shift
TODO

### Negative Integer in java
In Java, the integers are stored in the 2’s complement.

以下網址詳細介紹 :  
1. https://blog.codecritique.org/?p=357#:~:text=Two%E2%80%99s%20complement%20is%20used%20by%20Java%20to%20represent,range%20of%20%5B-2%2031%2C%202%2031%20%E2%80%93%201%5D.
2. https://stackoverflow.com/questions/30774640/what-is-a-twos-complement-integer

在java中有兩種right shift，分別是Signed and unsigned
### Signed Right Shift [>>]


# Bitwise Logical Operators
 AND(&), OR(|), XOR(^) , and NOT(~)  
<br>

## XOR(^) exclusive or、互斥或、異或
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

## OR(|) 或
```java
int i = 2; // 10
int j = 1; // 01

System.out.println(i | j); //3,  11 
```
##  AND(&)
```java
int i = 5; // 101
int j = 3; // 011

System.out.println(i & j); //1, 001
```

# 參考
[Bit Manipulation in Java – Bitwise and Bit Shift operations](https://www.vojtechruzicka.com/bit-manipulation-java-bitwise-bit-shift-operations/#:~:text=Java%20uses%20another%20approach%2C%20which%20is%20called%20two%27s,leftmost%20bit%20is%200%2C%20the%20number%20is%20positive.)
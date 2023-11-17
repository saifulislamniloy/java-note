# Stream (java.util.stream) 
#### [Offical Doc Link](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#builder--)

### Table of Content
- [allMatch](#allmatch)
- [Section 2](#section-2)
- [Section 3](#section-3)


## allMatch
#### Possible Output: true/false

Output - true
```
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9 ,10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;
        
boolean result = numbers.stream().allMatch(isNumberEven); /* result = false */
```

Output - false
```
List<Integer> numbers = Arrays.asList(2, 4, 6, 8, 10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

boolean result = numbers.stream().allMatch(isNumberEven); /* result = true */
```
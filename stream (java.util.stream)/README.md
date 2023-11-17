# Stream (java.util.stream) 
#### [Offical Doc Link](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#builder--)

### Table of Content
- [anyMatch](#anymatch)
- [allMatch](#allmatch)
- [noneMatch](#nonematch)
- [findAny](#findAny)



## anyMatch
#### Possible Output: true/false

Output - true
``` java
List<Integer> numbers = Arrays.asList(1, 3, 5, 7, 9, 10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

boolean result = numbers.stream().anyMatch(isNumberEven); /* result = true */
```

Output - false
``` java
List<Integer> numbers = Arrays.asList(1, 3, 5, 7, 9);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

boolean result = numbers.stream().anyMatch(isNumberEven); /* result = false */
```


## allMatch
#### Possible Output: true/false

Output - false
``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9 ,10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;
        
boolean result = numbers.stream().allMatch(isNumberEven); /* result = false */
```

Output - true
``` java
List<Integer> numbers = Arrays.asList(2, 4, 6, 8, 10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

boolean result = numbers.stream().allMatch(isNumberEven); /* result = true */
```



## noneMatch
#### Possible Output: true/false

Output - true
``` java
List<Integer> numbers = Arrays.asList(1, 3, 5, 7, 9);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

boolean result = numbers.stream().noneMatch(isNumberEven); /* result = true */
```

Output - false
``` java
List<Integer> numbers = Arrays.asList(1, 3, 5, 7, 9, 10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

boolean result = numbers.stream().noneMatch(isNumberEven); /* result = false */
```



## findAny
#### Possible Output: (with value/empty) optional

Output - with value optional
``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

Optional<Integer> result = numbers.stream().filter(isNumberEven).findAny(); /* result = value (2 or any even) */

```

Output - empty optional
``` java
List<Integer> numbers = Arrays.asList(1, 3, 5, 7, 9);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

Optional<Integer> result = numbers.stream().filter(isNumberEven).findAny(); /* result = empty */
```



## findFirst
#### Possible Output: (with value/empty) optional

Output - with value optional
``` java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

Optional<Integer> result = numbers.stream().filter(isNumberEven).findFirst(); /* result = value (2) */

```

Output - empty optional
``` java
List<Integer> numbers = Arrays.asList(1, 3, 5, 7, 9);

Predicate<Integer> isNumberEven = number -> number % 2 == 0;

Optional<Integer> result = numbers.stream().filter(isNumberEven).findFirst(); /* result = empty */
```

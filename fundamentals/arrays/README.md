# Array
Array is a data structure.


### Table of Content
- [Array](#array)
    - [Table of Content](#table-of-content)
  - [Array Initialization](#array-initialization)
  - [Array Iteration](#array-iteration)

## Array Initialization

``` java
/* Way 1 */
int[] arr = new int[5]; /* arr.length = 5, initialized with 0 */

/* Way 2 */
int[] arr = new int[]{1, 3, 5, 7, 9};
```



## Array Iteration

``` java
/* Way 1 - indexed for loop*/
int[] arr = new int[]{1, 3, 5, 7};

for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}

/* Way 2 - enhanced for loop */
int[] arr = new int[]{1, 3, 5, 7};

for (int element : arr) {
    System.out.println(element);
}


/* Way 3 - while loop */
int[] arr = new int[]{1, 3, 5, 7};

int i = 0, arrLength = arr.length;
while (i < arrLength) {
    int element = arr[i];
    System.out.println(element);
    i++;
}
```
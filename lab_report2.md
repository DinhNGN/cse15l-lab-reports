# Lab Report 2 - Servers & Bugs
## Part 1 ~ StringServer

### The code for my StringServer.java: 

![image](https://user-images.githubusercontent.com/122498399/215599058-88d50bb9-7afa-4f3c-b1a6-f54cf33cbf67.png)

### The examples of string responses:

![image](https://user-images.githubusercontent.com/122498399/215600273-5a0dcb8a-969e-4448-b250-3a8cb5ef0fe2.png)
- The example above calls on the handleRequest method. In this method, the program would evaluate the contents of the path following "/". Since there exists
more to the path than just ending at "/", the program will evaluate what follows to check if it's a valid input for "/add-messages", & if is so & it contains
a valid input, the input will be returned & displayed on the page as shown. 

![image](https://user-images.githubusercontent.com/122498399/215601409-da26a745-929b-4d60-9a9c-5d08a8192544.png)
- The example above much like the previous calls on the handleRequest method. In this method, the program would evaluate
the contents of the path following "/". Since there exists more to the path than just ending at "/", the program will evaluate what follows
to check if it's a valid input for "/add-messages", & if is so & it contains a valid input, the input will be returned & displayed on the page as shown.

## Part 2 ~ Bugs

### Failing Test: <br/>
        public void testReversed2() {
            int[] input2 = { 1, 2, 3, 4, 5 };
            assertArrayEquals(new int[]{ 5, 4, 3, 2, 1}, ArrayExamples.reversed(input2));
        }

### Passing Test: <br/>
        public void testReversed() {
          int[] input1 = { };
          assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
        }

### Symptom:
![image](https://user-images.githubusercontent.com/122498399/215609711-d7feb556-4381-4e86-8b4d-396ae794e324.png)

### The Bug Fixed(Before & After):
- Before: <br/>
        static int[] reversed(int[] arr) {
          int[] newArray = new int[arr.length];
          for(int i = 0; i < arr.length; i += 1) {
          arr[i] = newArray[arr.length - i - 1];
          }
          return arr;

- After: <br/>
        static int[] reversed(int[] arr) {
          int[] newArray = new int[arr.length];
          for(int i = 0; i < arr.length; i += 1) {
          newArray[i] = arr[arr.length - i - 1];
          }
          return newArray;
        }

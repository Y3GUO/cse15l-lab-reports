## Lab Report 3
Yutong Guo<br>
A16269813<br>
### PART 1
The reverseInPlace method in the Array methods.
1. A failure-inducing input would be:
   ``` {java}
   @Test
   public void testReverseInPlace2() {
    int[] input1 = { 3, 4, 5 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 5, 4, 3 }, input1);
   }
   ```
2. A code that does not induce failure:
   ```{java}
   @Test
   public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
   }
   ```
3. The symptom:
   ![Image](pic1.png)<br>

4. The bug: <br>
   Before:
   ```{java}
   static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
   }
   ```
   
   After:
   ```{java}
   static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i++) {
        int temp = arr[i];
        arr[i] = arr[arr.length - i - 1];
        arr[arr.length - i - 1] = temp;
    }
   }
   ```
   <br>
   The original bug is because the array is dynamically changing as we are setting the second half of the array equal to their original value because we set the first part of the array equal to the second half, so when we reach the second half of the array, the data was overwritten and we lost the data of the first half of the array.
### PART 2
We will explore the command ```less```. Here I will explore 4 different command line options.
1. -E <br>
   By using this command line option, ```less``` automatically exits upon reaching the end of the file. This is pretty easy to understand, here are two examples:<br>
   Example 1:<br>
   

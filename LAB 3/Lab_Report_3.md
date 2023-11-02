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

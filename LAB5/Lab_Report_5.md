## Lab Report 4
Yutong Guo<br>
A16269813<br>
### Part 1
1. **Original Post**:
Title: Issue with `ListExamples.merge` Method Not Merging Lists Correctly
Hey, I'm working on this `ListExamples` class, specifically the merge method. It's supposed to merge two sorted lists into a single sorted list. However, I'm running into an issue where the method doesn't seem to be merging the lists correctly. Here's a screenshot of my test case and the output:<br>
**Test**:<br>
![Image](test.png)<br>
**Result**:<br>
![Image](result.png)<br>
For the first test, it merges lists with elements ["x", "y"] and ["a", "b"] just fine. However, when it tries to merge ["a", "b", "c"] with ["c", "d", "e"], it gives us a 500 ms timeout.<br>
I'm guessing there's an issue when both lists contain a common element, which in our case is "c". This might be causing the merge function to enter an infinite loop. Has anyone encountered a similar problem or can spot where the error might be happening in the merge method?<br>
2. **TA's Response**:<br>
Hello,<br>
Great job on setting up your test cases and noticing the timeout during the second test. The fact that testMerge2 is timing out is indeed indicative of an infinite loop. Given that your first test passes but the second fails, we should look closely at what differs between the two scenarios.<br>
You’ve made a good observation regarding the common element "c" in both lists for testMerge2. In a merge operation, it's critical that each element is only processed once, even if it appears in both lists. If the code mistakenly continues to compare the same pair of elements without moving forward, it could result in an infinite loop.<br>
Could you insert a few print statements inside the merge method to print out the values of index1 and index2 before and after you expect them to change? Like: `System.out.println("index1: " + index1 + ", index2: " + index2);`. This will help you solve the problem, feel free to reach out for more questions!
3. **Code after advice**:

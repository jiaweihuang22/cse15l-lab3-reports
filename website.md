Part 1
=========


* A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)


```
@Test
  public void test1() {
    int[] input1 = {3,3,3,1};
    assertArrayEquals(new int[]{1,3,3,3}, ArrayExamples.reversed(input1));
  }
}
```


* An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)


```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```


* The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)


![Image](Output.png)


* The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)


```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```


```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return newArray;
}
```


* Briefly describe why the fix addresses the issue.


The bug was that elements were being changed/added in arr from newArray and not vice versa, it also returned the old array, not newArray


Part 2
=========


**Command: Find** 


**First Example**


`find -name <files>`


**1:**


![Image](Example11.png)


This command searches for both files and directories with the given name. It is useful because you can look for specific files when there are many files within the folders.


**2:**


![Image](Example12.png)


This command searches for both files and directories with the given name. It is useful because you can look for specific files when there are many files within the folders.


**Second Example**


`find -type f -name <files>`


**1:**


![Image](Example21.png)


This command searches for files only with the given name. It is useful because it will exclude the directory in the output so that the output is easier to see.


**2:**


![Image](Example22.png)


This command searches for files only with the given name. It is useful because it will exclude the directory in the output so that the output is easier to see.


**Third Example**


`find <directory> -size +<number>`


**1:**


![Image](Example31.png)


This command searches for files based on the given size. It is useful because it will exclude files that is smaller than our expected size such as empty files in our output.


**2:**


![Image](Example32.png)


This command searches for files based on the given size. It is useful because it will exclude files that is smaller than our expected size such as empty files in our output.


**Fourth Example**


`find <directory> -mtime -<number>`


**1:**


![Image](Example41.png)


This command searches for the directory based on how many days(the number we give) it was modified. It is useful because in the situation where we only want the files we just modified yesterday we can put the number as 1 which in the output, it will exclude all other files except the ones we modified yesterday.


**2:**


![Image](Example42.png)


This command searches for the directory based on how many days(the number we give) it was modified. It is useful because in the situation where we only want the files we just modified yesterday we can put the number as 1 which in the output, it will exclude all other files except the ones we modified yesterday.


**Cited Work**

`https://linuxhandbook.com/find-command-examples/`



https://chat.openai.com/share/ccd8c3b8-0511-4ab3-b970-152ec95b1ab1

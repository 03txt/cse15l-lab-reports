# Lab 3: Bugs and Commands 
## Part One: Bugs 
### Failure inducing input for ```reverseInPlace()```
```
@Test
public void testReverseInPlaceOdd()
{
  int[] input1 = {1,2,3};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{3,2,1}, input1};
}
```
### Non-failure inducing input for ```reverseInPlace()```
```
@Test
public void testReverseInPlaceOdd()
{
  int[] input1 = {};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{}, input1};
}
```
### Symptoms: 
![image](fail1.png)
![image](fail2.png)

### Code with bug: 
```
static void reverseInPlace(int[] arr)
  {
      for(int i = 0; i < arr.length; i += 1)
     {
        arr[i] = arr[arr.length - i - 1];
    }
  }
```

### Fixed: 
```
static void reversedInPlace(int[] arr)
{
  for (int i = 0; i < arr.length / 2; i++)
  {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp; 
  }

}
```
## Part Two: Researching Commands
## 'grep'

- '-i' (ignore case): This command option ignores the case of the the patter it is searching! For example: 





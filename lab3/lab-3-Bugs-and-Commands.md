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

## Code with bug: 
```

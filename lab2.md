# Lab2

![image](https://user-images.githubusercontent.com/98847913/234123301-ca418b6a-9906-419d-9393-67469ac1d3a5.png)

![image](https://user-images.githubusercontent.com/98847913/234123427-7db36b1c-f627-4d2b-85a9-c90e047b62d9.png)

```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

```
  @Test
  public void testReversedShortArray() {
    int[] input1 = {1,2,3 };
    assertArrayEquals(new int[]{3,2,1 }, ArrayExamples.reversed(input1));
  }
```

![image](https://user-images.githubusercontent.com/98847913/234126813-c19f4d05-9aba-4d3f-915b-dc5a7ce76c7b.png)

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
      newArray[arr.length - i - 1]=arr[i];

    }
    return newArray;
  }
  ```

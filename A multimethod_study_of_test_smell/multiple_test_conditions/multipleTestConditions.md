## Multiple Test Conditions

```java
public void testMultipleValueSets(){
  // Set Up Fixture
  Calculator sut = new Calculator();
  TestValues[] testValues = {
    new TestValues(1,2,3),
    new TestValues(2,3,5),
    new TestValues(3,4,8),
    new TestValues(4,5,9)
  };
  for (int i = 0; i < testValues.length; i++){
    TestValues values = testValues[i];
    int actual = sut.calculate( values.a, values.b);
    assertEquals(message(i), values.expectedSum, actual);
  }
}

private String message(int i) {
  return "Row "+ String.valueOf(i);
}
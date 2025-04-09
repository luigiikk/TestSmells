## Branch To Assumption Anti-Pattern

```java
void Test(int i, int j) {
  if (i < 0)
  PexAssume.IsTrue(j > 0);
  ...
}
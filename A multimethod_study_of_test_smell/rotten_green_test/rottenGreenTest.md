## Rotten Green Test

```java
@Test
public void testListWindowsNewBucket() throws Exception {
  . . .
  BucketLeapArray leapArray = new BucketLeapArray(sampleCount,
          intervalInMs);
  . . . .
  List<WindowWrap<MetricBucket>> list = leapArray.list();
  for (WindowWrap<MetricBucket> wrap : list) {
    assertTrue(windowWraps.contains(wrap));
  }
  . . . .
}
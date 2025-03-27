## Two for the price of one (Java)

```java
private LocalDateTime now = LocalDateTime.now();
private LocalDateTime tomorrow = LocalDateTime.plus(1, DAYS);
private LocalDateTime yesterday = LocalDateTime.minus(1, DAYS);

@Test
public void dateComparisonWorksForPastAndFuture() {
    assertDateComparison(now, tomorrow, "is in the future");
    assertDateComparison(now, yesterday, "is in the past");
}

private void assertDateComparison(LocalDateTime baseline,
                                LocalDateTime compare,
                                String expected) {
    assertEquals(expected, MyDates.describe(baseline, compare));
}
```  




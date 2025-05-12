## Missed Skip Rotten Green Test

```java
@Test
    public void testNormalizedKeysGreatSmallAscDescHalfLenght(){
    TypeComparator<T> comparator = getComparator(true);
    if (not(comparator.supportsNormalizedKey())){
        return;
    }
    testNormalizedKeysGreatSmall(true, comparator,true);
    testNormalizedKeysGreatSmall(false, comparator,true);
    }
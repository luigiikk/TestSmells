## Skip Rotten Green Test

```java
@Test public void testNormalizedKeyReadWriter(){
   . . .
   TypeComparator <T> comp1 = getComparator(true);

   if(!comp1.supportsSerializationWithKeyNormalization()){
    return ;
   }
   . . .
   assertTrue(comp1.compareToReference(comp2) == 0);
   . . .
}
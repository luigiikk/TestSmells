## Test Smell (Java)

```java
import java.util.Random;

@Test 
public void testBasic() throws Exception {
    final Random random = new Random();
    if (random.nextInt(100) < 10) {
        doLocking(lock.writeLock(), concurrentCount, maxConcurrentCount, random, 1);
        writeCount.incrementAndGet();
    }
}
```

## Test Smell (JavaScript)

```javascript
it('should generate a random user ID', () => {
    const userId = generateRandomUserId(); 
    expect(userId).toHaveLength(10); 
});
```

## Parameter Order Wrong (Java)

### Test Code:

```java
import static org.junit.Assert.assertEquals;

@Test 
public void test01ColumnFormatUIR() throws LibrecException {
    TextDataModel dataModel = new TextDataModel(conf);
    dataModel.buildDataModel();
    assertEquals(getDataSize(dataModel), 13); 
}
```

### API Usage:

```java
static void assertEquals(double expected, double actual)
```

## Parameter Order Wrong (JavaScript)

```javascript
it('should check if user name is correct', () => {
    const user = { name: 'John Doe' };
    
    expect('John Doe').toBe(user.name); // ❌ Ordem errada dos parâmetros
});
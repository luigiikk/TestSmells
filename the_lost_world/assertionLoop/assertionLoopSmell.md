## Test Smell (Java)

```java
@Test 
public void testInvalidChar() {
    String[] invalidPatterns = new String[]{"", "1", "ABC", "#x0001 - #x - #x0000", "#x0000 #x0022"};
    for (String i : invalidPatterns) {
        assertThrows(IllegalArgumentException.class, () -> {
            myFilter.add(i);
        });
    }
}
```

## Test Smell (JavaScript)

```javascript
test("should return all users with valid names", () => {
    const users = getUsers(); // Suponha que retorna uma lista de usuários [{ name: "Alice" }, { name: "Bob" }]

    for (let user of users) {
        expect(user.name).toBeDefined(); // ❌ Problema: Se falhar, não sabemos qual usuário causou o erro
    }
});

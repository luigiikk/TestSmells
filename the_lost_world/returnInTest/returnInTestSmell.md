## Return in Test (Java)

```java
@Path("/mode/test")
@GET
@Test 
public Result testAnnotatedTestRoute() {
    return Results.text().render("test mode works.");
}
```

## Return in Test (JavaScript)

```javascript
test("should return a user", () => {
    const user = getUser();
    return user; // ❌ Problema: Testes não devem retornar valores
});
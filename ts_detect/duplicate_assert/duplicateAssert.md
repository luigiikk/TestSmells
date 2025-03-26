## Duplicate Assert (JavaScript)

```javascript
test("should return the correct username", () => {
  const user = new User("Jhon", 30);
  
  expect(user.name).toBe("Jhon");
  expect(user.name).toBe("Jhon"); 
});

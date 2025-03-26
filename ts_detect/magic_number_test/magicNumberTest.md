## Magic Number Test (JavaScript)

```javascript
test("should check if user is adult", () => {
  const user = new User("John", 25);
  expect(user.age >= 18).toBe(true);
});
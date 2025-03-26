## Eager Test (JavaScript)

```javascript
test("should handle user operations", () => {
  const user = new User("Jhon", 30);

  user.updateName("Bob");
  expect(user.name).toBe("Bob");

  user.updateAge(35);
  expect(user.age).toBe(35);

  user.activate();
  expect(user.isActive).toBe(true);
});

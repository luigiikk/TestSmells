## Lazy Test (JavaScript)

```javascript
test("should handle user actions", () => {
  const user = new User("Alice");

  user.login();
  expect(user.isLoggedIn).toBe(true);

  user.updateProfile({ age: 25 });
  expect(user.profile.age).toBe(25);

  user.logout();
  expect(user.isLoggedIn).toBe(false);
});

## Conditional Test Logic (JavaScript)

```javascript
test("should validate user role", () => {
  const user = getUser();

  if (user.role === "admin") {
    expect(user.hasAccess).toBe(true);
  } else {
    expect(user.hasAccess).toBe(false);
  }
});

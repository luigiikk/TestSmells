## Exception Handling (JavaScript)

```javascript
test("should throw an error when the user is not found", () => {
  try {
    findUserById(999);
  } catch (error) {
    expect(error.message).toBe("User not found");
  }
});
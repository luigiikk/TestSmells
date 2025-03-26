## Assertion Roulette (JavaScript)

```javascript
test("should validate user data", () => {
    const user = getUser();
    expect(user.name).toBe("Jhon"); 
    expect(user.age).toBe(25);
    expect(user.email).toBe("jhondoe@email.com"); 
});
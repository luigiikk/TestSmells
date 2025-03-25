## Test Smell (Java)

### Production Code:

```java
private boolean checkTime(char h0, char h1, char m0, char m1, char s0, char s1) {
    if (h0 == '0') {
        if (h1 < '0' || h1 > '9') {
            return false;
        }
        ...
        return true;
    }
}
```

### Test Code:

```java
Class<?> c = Reflector.forName("com.alibaba.fastjson.parser.JSONScanner");
Method m = c.getDeclareMethod("checkDate", Reflector.
forName("char"), Reflector.forName("char"), Reflector.
forName("char"), Reflector.forName("char"), Reflector.
forName("char"), Reflector.forName("char"), Reflector.
forName("int"), Reflector.forName("int"));
m.setAcessible(true);
boolean retval = (Boolean)m.invoke(null, y0, y1, y2, y3, M0, M1, d0, d1);
Assert.assertEquals(true, retval);
```

## Test Smell (JavaScript)

```javascript
class User {
    constructor(name) {
        this.name = name;
    }

    // Método privado (indicativo com _)
    _calculateDiscount() {
        return 0.1; // Exemplo simples
    }

    getDiscountedPrice(price) {
        return price - price * this._calculateDiscount();
    }
}

it('should calculate discount correctly', () => {
    const user = new User('John Doe');
    
    // Acessando diretamente o método privado (violando o encapsulamento)
    expect(user._calculateDiscount()).toBe(0.1); // Testando diretamente um método privado
});
```

## Test Body Is Somewhere Else

```java
@Test
public void hasCorrectFoo() {
  checkFoo();
}

private static checkFoo() {
  Foo foo = service.getFoo();
  assertThat(foo.getBar()).isEqualTo("baz");
}
## Envolve Or

```java
public class TransactionTest {
  @Test
  public void shouldRecognizeTransactionsWithZeroValueAsInvalid() {
    //given
    Transaction tx = new Transaction(BigDecimal.ZERO,
    new InternalUser());
    //when
    boolean actual = tx.validate();
    //then
    assertThat(actual).isFalse();
  }

  @Test
  public void shouldRecognizeTransactionWithNegativeValueAsInvalid() {
    //given
    Transaction tx = new Transaction(BigDecimal.ONE.negate(),
    new InternalUser());
    //when
    boolean actual = tx.validate();
    //then
    assertThat(actual).isFalse();
  }
}
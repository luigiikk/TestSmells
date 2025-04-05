## Hard Coded Test Data

```java
public void testAddItemQuantity_severalQuantity_v12(){
    //  Setup Fixture
    Customer cust = createACustomer(new BigDecimal("30"));
    Product prod = createAProduct(new BigDecimal("19.99"));
    Invoice invoice = createInvoice(cust);
    // Exercise SUT
    invoice.addItemQuantity(prod, 5);
    // Verify Outcome
    LineItem expected = new LineItem(invoice, prod, 5,
            new BigDecimal("30"), new BigDecimal("69.96"));
    assertContainsExactlyOneLineItem(invoice, expected);
}










## Code Pollution

```java
// In main code
public class OrderRepository
{
    public void Save(Order order)
    {
        /* ... */
    }

    public Order GetById(long id)
    {
        /* ... */
    }
}

// in test code
public void Some_integration_test()
{
    // Arrange
    var repository = new OrderRepository();
    var service = new OrderService(repository);
    long customerId = 42;

    // Act
    service.DoSomething(customerId);

    // Assert
    IReadOnlyList<Order> orders = repository.GetByCustomerId(customerId); // Code added for the use in this unit test
    /* validate orders */
}
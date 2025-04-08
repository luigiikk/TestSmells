## Asynchronus Test

```java
public class RequestHandlerThreadTest extends TestCase {
  private static final int TWO_SECONDS = 3000;
  public void testWasInitialized_Async() throws InterruptedException {
    RequestHandlerThread sut = new RequestHandlerThread();

    sut.start();

    Thread.sleep(TWO_SECONDS);
    assertTrue(sut.initializedSuccessfully());
  }

  public void testHandleOneRequest_Async() throws InterruptedException {
    RequestHandlerThread sut = new RequestHandlerThread();
    sut.start();

    enqueueRequest(makeSimpleRequest());

    Thread.sleep(TWO_SECONDS);
    assertEquals(1, sut.getNumberOfRequestsCompleted());
    assertResponseEquals(makeSimpleResponse(), getResponse());
  }
}
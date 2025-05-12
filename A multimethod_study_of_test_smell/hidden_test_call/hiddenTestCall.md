## Hidden Test Call

```java
[TestFixture]
public class HiddenTestCall {
  private LogAnalyzer logan;

  [Test]
  public void CreateAnalyzer_GoodNameAndBadNameUsage() {
    logan.new LogAnalyzer();
    logan.Initialize();
    bool valid = logan.IsValid("abc");
    Assert.That(valid, Is.False);
    CreateAnalyzer_GoodFileName_ReturnsTrue();
  }

  [Test]
  public void CreateAnalyzer_GoodFileName_ReturnsTrue() {
    bool valid = logan.IsValid("abcdefg");
    Assert.That(valid. Is.True);
  }
}
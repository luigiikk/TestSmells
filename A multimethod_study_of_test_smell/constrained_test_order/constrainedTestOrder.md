## Constrained Test Order

```java
[TestFixture]
public class IsolationsAntiPatterns
{
  private LogAnalyzer logan;

  [Test]
  public void CreateAnalyzer_BadFileName_ReturnsFalse()
  {
    logan = new LogAnalyzer();

    logan.Initialize();

    bool valid = logan.IsValid("abc");

    Assert.That(valid, Is.False);
  }

  [Test]
  public void CreateAnalyzer_GoodFileName_ReturnsTrue()
  {
    bool valid = logan.IsValid("abcdefg");

    Assert.That(valid, Is.True);
  }

}
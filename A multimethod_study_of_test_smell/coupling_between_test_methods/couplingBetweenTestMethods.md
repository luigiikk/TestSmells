## Coupling Between Test Methods

```java
public final class MetricsTest {
  private File temp;
  private Folder folder;
  @Before
  public void prepare() {
    this.temp = Files.createTempDirectory("test");
    this.folder = new DiscFolder(this.temp);
    this.folder.save("first.txt", "Hello, world!");
    this.folder.save("second.txt", "Goodbye!");
  }
  @After
  public void clean() {
    FileUtils.deleteDirectory(this.temp);
  }
  @Test
  public void calculatesTotalSize() {
    assertEquals(22, new Metrics(this.folder).size());
  }
  @Test
  public void countsWordsInFiles() {
    assertEquals(4, new Metrics(this.folder).wc());
  }
}
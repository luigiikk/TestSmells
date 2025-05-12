## Everything is A Property


```java
class ParagraphAnalyzerTest {
    private String analyzed;
    private ParagraphAnalyzer analyzer = new ParagraphAnalyzer();

    @Test
    void nouns() {
        analyzed = analyzer.justNouns("This is a word");
        assertThat(analyzed).isEqualTo("word");
    }

    @Test
    void verbs() {
        analyzed = analyzer.justVerbs("This is a word");
        assertThat(analyzed).isEqualTo("is");
    }

    @Test
    void ends() {
        analyzed = analyzer.first("This is a word");
        assertThat(analyzed).isEqualTo("This");

        analyzed = analyzer.last("This is a word");
        assertThat(analyzed).isEqualTo("words");
    }
}
## The First And Last Rite (Java)

```java
@Test
public void connectionWorks() {
    database = openDatabase();

    database.healthCheck();

    database.close();
}

@Test
public void countRows() {
    database = openDatabase();

    assertThat(database.countAll())
    .isEqualTo(0);

    database.close();
}
```  




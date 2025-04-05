## Hard Coded Values

```php
public function testGetTranslationFileTimestamp()
{
    $this->fileManagerMock->expects($this->once())
        ->method('getTranslationFileTimestamp')
        ->willReturn(1445736974);
    $this->assertEquals(1445736974, $this->model->getTranslationFileTimestamp());
}
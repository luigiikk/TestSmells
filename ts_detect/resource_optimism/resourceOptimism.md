 ## Resource Optimism (JavaScript)

```javascript 
 test('should read the file contents', () => {
    const data = fs.readFileSync(path, 'utf-8');
    expect(data).toBe('Hello, World!');
  });
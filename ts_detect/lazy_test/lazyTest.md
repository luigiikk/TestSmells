## Lazy Test (JavaScript)

```javascript
// Production code ( circle.js )
 const PI = 3.14159265359;

 export function area ( radius ) {
 return ( radius ** 2) * PI;
 }

 module.exports = function circumference ( radius ) {
 return 2 * radius * PI;
 }

 import { area , circumference } from './ circle.js ';

 describe ('Test creation file ', () => {
 it('create a text ', () => {
 const PI = 3.14159265359;
 const r = 3;
 assert.equal ( area (r) , r ** 2) ;
 }) ;
 }) ;

 describe ('Test updating file ', () => {
 it('update a text ', () => {
 const PI = 3.14159265359;
 const r = 3;
 assert.equal ( area (r) , r ** 2) ;
 assert.equal ( circumference (r) , 2 * PI * r);
 assert.equal ( circumference (r) , 2 * PI * r);
 }) ;
}) ;

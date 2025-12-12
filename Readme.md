### Code for collecting form data without using usestate
```js
const handleSubmit = (e) => {
  e.preventDefault();
  const formData = new FormData(e.currentTarget)
  const data = Object.fromEntries(formData);
  console.log(data);
  // reset form
  e.target.reset();
}
```
### React-router-dom
```js
import { create
```

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
**Router.jsx**
```js
import { createBrowserRouter } from "react-router-dom";
import Login from "./Pages/Login";
import App from "./App";
import Register from "./pages/Register";

export const Router = createBrowserRouter(
  [
    {path:'/', element: <App />, children: [
      {path: 'profile', element: <></>}
    ]},
    {path: '/login', element: <Login />},
    {path: '/register', element: <Register />}
  ]
);
```
**main.jsx**
```js
import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client'
import './index.css'

import { RouterProvider } from 'react-router-dom';
import { Router } from './Router.jsx';


createRoot(document.getElementById('root')).render(
  <StrictMode>
    <RouterProvider router={Router} />
  </StrictMode>,
)
```

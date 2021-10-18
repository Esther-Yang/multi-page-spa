# Multi Page SPA

A React App that used to demonstrate multi-page spa.

# Feature

- Act like a multi-page application using React Router.
- Two pages
  - Welcome page: shows "The Welcome Page".
  - Products page: shows "The Products Page" and a list of products.
- \*The CSS is not complete.

# Procedure

1. Install React Router.

```
npm install react-rounter-dom
```

2. Used `Route` from `react-router-dom`.

```
//App.js
<Route path='/welcome`>
    <Welcome/>
</Route>
```

3. Used `<BrowserRouter>` from `react-router-dom`.

```
//index.js
<BrowserRouter><App/></BrowserRouter>
```

4. Used `<Link>` from `react-router-dom` which will be rendered to `<a href="#">`. The reason we do not use `<a>` directly is because it will automatically send html request to load a whole page, and all the states will gone.

```
//MainHeader.js
<Link to="/welcome">Welcome</Link>
```

5. Used `<NavLink>` from `react-router-dom` to have active links highlighted at the nav bar.

```
//MainHeader.js
<NavLink activeClassName={classes.active} to="/welcome">

//MainHeader.module.css
.header a.active
```

6. Used Dynamic Routes with Params. Syntax is a **colon followed by identifier**.

```
<Route path="product-detail/:productId">
```

7. Extracted Route Params with `useParams`, a custom hook from `react-router-dom`.

```
//ProductDetail.js
const params = useParams();
console.log(params.productId);
```

8. Used `<Switch>` to wrap `<Route>`: to have only one active link at a time.

9. Used `exact` prop in `<Route>`: to have exact match.

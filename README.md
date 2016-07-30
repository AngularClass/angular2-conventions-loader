<p align="center">
  <a href="http://courses.angularclass.com/courses/angular-2-fundamentals" target="_blank">
    <img width="438" alt="Angular 2 Fundamentals" src="https://cloud.githubusercontent.com/assets/1016365/17200649/085798c6-543c-11e6-8ad0-2484f0641624.png">
  </a>
</p>

___

# Angular 2 Conventions Loader
Allow default for `@Component` metadata for Angular 2

`npm install @angularclass/conventions-loader --save-dev`

```js
{
  test: /\.ts$/,
  loaders: [
    'ts-loader',
    '@angularclass/conventions-loader'
  ]
},
```

Given this simple Component example
`app.js`

```typescript
@Component({})
export class App {
}
```
Webpack will change the code
`app.js`

```typescript
@Component({
  selector: "app",
  styles: [require("./app.css")],
  template: require("./app.html")
})
export class App {
}
```
this is assuming you have coresponding files next to the component. You may overwrite the selector at anytime by providing one. If the selector and the component file name does not match then the coresponding css/template file with the selector will be injected.


___

enjoy — **AngularClass**

<br><br>

[![AngularClass](https://cloud.githubusercontent.com/assets/1016365/9863770/cb0620fc-5af7-11e5-89df-d4b0b2cdfc43.png  "Angular Class")](https://angularclass.com)
##[AngularClass](https://angularclass.com)
> Learn AngularJS, Angular 2, and Modern Web Development from the best.
> Looking for corporate Angular training, want to host us, or Angular consulting? patrick@angularclass.com

___

Apache-2.0

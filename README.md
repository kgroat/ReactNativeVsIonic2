# React Native vs. Ionic 2

### Language
##### React Native
###### JSX
React's JSX syntax allows for your template and JavaScript to coexist.  You don't have to maintain your XML/HTML and JS separately, but notably, it is first and foremost JavaScript, simply with the ability to create objects that compile down to DOM tree representations.  In React Native, these represent not HTML elements, but XML elements that themselves represent native components.

##### Ionic 2
###### TypeScript
Like JSX, TypeScript is first and foremost JavaScript.  If you please, you can use the language without utilizing its powerful type system.  Even if you choose not to use types, you still get the utility of the powerful transpiler, which supports many ES2016 features, and even some features beyond ES2016.
###### HTML
The templating engine built into Angular 2 is more readable than the one built into Angular 1.x; these templates are no longer confusing, but are actually [highly declarative and easy to follow](https://angular.io/docs/ts/latest/guide/template-syntax.html).

### Speed
##### React Native
With the speed of a native application, React Native is the clear winner here.  It has the performance of a native application because it truly is one.
##### Ionic 2
Ionic 2 might be a hybrid application, but its performance is unrivalled in the hybrid realm.  Being built on top of Angular 2, you get the performance of the newly rebuilt framework.  In metrics of speed, [everything is faster than Angular 1.x](https://auth0.com/blog/more-benchmarks-virtual-dom-vs-angular-12-vs-mithril-js-vs-the-rest/).  Luckily, Ionic 2 is built on top of Angular 2, whose speed is more in line with modern web frameworks.  Because of this, and because of the speed of modern mobile browsers, the experience of an Ionic 2 application is not a far cry from a native application, as was the case for so long -- even while using Ionic 1.

### Styling
##### React Native
React Native comes with no default styling, and is a blank slate by which to craft your application.  You can pull in CSS libraries like [Bootstrap](http://getbootstrap.com/) and [Materialize](http://materializecss.com/), or you can build your own custom CSS.  Unfortunately, because React Native has to compile all of this down to native instructions, the CSS you can use is a subset of the full styling language.
##### Ionic 2
Ionic 2 comes with a fully-fleshed-out CSS library to give the styling users expect based on which operating system they are using.  Depending on whether the user's device is running iOS, Android, or Windows, the buttons, tabs, and other components appear in a manner very similar to their native counterparts on that OS.  That being said, this doesn't mean that the CSS is not extensible, or that you even have to use the built-in CSS.  You can, if you so choose, write your own styles to make your app look exactly the way you want.  Ionic 2 also comes with SASS support out-of-the box.


### Additional Considerations
##### Ionic 2
###### Observables
Being built on top of Angular 2, asyncronous functionality is handled using [Reactive Extensions](https://github.com/Reactive-Extensions/RxJS).  RxJs gives you the power of `Observables`, which allow their user to treat any data source as though it is a stream.  You can use functions such as `.map()` and `.reduce()` which act similarly to their `Array` counterparts to manipulate the data coming through the stream before you `.subscribe()`.  Angular 2 makes Observables first-class citizens, handling subscriptions and display of asynchronous data.
###### CLI
Ionic comes with a CLI built to ease the development and testing process.  By typing `ionic start --v2 MyApp`, it will generate an app called MyApp using an existing project from which to get started.  Once there, you can use `ionic generate page home` to create a page called home.  There are [many generators](https://ionicframework.com/docs/v2/cli/generate/) built into the CLI which allow you to grow your application easily.
###### Tooling
Along with the CLI, [Ionic Cloud](http://ionic.io/) gives you the ability to perform many tasks very easily.  Among the things Ionic Cloud allows you to do are:
* [Build and sign your application](http://docs.ionic.io/services/package/) for either iOS or Android with a single command
* Create and maintain a user/permission tree with [OAuth 2.0 support for Google, Facebook, and others](http://docs.ionic.io/services/auth/#authentication-providers)
* Send [push notifications](http://docs.ionic.io/services/push/) to devices
* Get application analytics
* Get, review, and assess feedback from testers and users
* Automatically [deploy new code](http://docs.ionic.io/services/deploy/) to users without need to reinstall from the App Store
###### Beyond Hybrid
Because Ionic 2 is built using true HTML and CSS, you have the option of deploying it as a web application.  You can turn your Ionic 2 application into a standalone web UI, and even potentially turn it into a Progressive Web App using a `ServiceWorker` and `manifest.json` file.  Even if you don't plan to deploy it as a web application, you can still utilize the powerful capabilities of the `ServiceWorker` in the hybrid native experience by doing such things as precaching, sending native-like push notifications, or any of the many other things you can accomplish with the technology.





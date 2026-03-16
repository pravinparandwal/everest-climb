Difference between map and 1foreach angular?
•	The forEach() method is primarily used for iterating over array elements and executing a provided function once for each array element. 
•	It doesn’t create a new array and doesn’t return anything. 
•	It’s mainly used when you want to perform an operation on each element of the array without creating a modified version of the array.
•	forEach() will allow a callback function to mutate the current array.

const numbers = [1, 2, 3, 4];

numbers.forEach((number) => {
  console.log(number * 2);
});

•	The map() method is also used for iterating over array elements, but its main purpose is to create a new array by applying a provided function to each element of the original array. 
•	It returns a new array with the results of applying the function to each element.

const numbers = [1, 2, 3, 4];
 
const doubledNumbers = numbers.map((number) => {
  return number * 2;
})
console.log(doubledNumbers);

What is Bazel tool?
•	Bazel is a powerful build tool developed and massively used by Google 
•	And it can keep track of the dependencies between different packages and build targets.
•	In Angular8+, you can build your CLI application with Bazel. 
Note: The Angular framework itself is built with Bazel.

What are different types of 1compilation in Angular?
Angular offers two ways to compile your application,
1.	Just-in-Time (JIT)
2.	Ahead-of-Time (AOT)

What is JIT?
Just-in-Time (JIT) is a type of compilation that compiles your app in the browser at runtime. JIT compilation is the default when you run the ng build (build only) or ng serve (build and serve locally) CLI commands. i.e, the below commands used for JIT compilation,
ng build
ng serve

What is 1AOT?
Ahead-of-Time (AOT) is a type of compilation that compiles your app at build time. For AOT compilation, include the --aot option with the ng build or ng serve command as below,
ng build --aot
ng serve –aot

Note: The ng build command with the --prod meta-flag (ng build --prod) compiles with AOT by default.

Why do we need compilation process?
The Angular components and templates cannot be understood by the browser directly. Due to that Angular applications require a compilation process before they can run in a browser. For example, In AOT compilation, both Angular HTML and TypeScript code converted into efficient JavaScript code during the build phase before browser runs it.

What are the advantages with AOT?
Below are the list of AOT benefits,
•	Faster rendering: The browser downloads a pre-compiled version of the application. So it can render the application immediately without compiling the app.
•	Fewer asynchronous requests: It inlines external HTML templates and CSS style sheets within the application javascript which eliminates separate ajax requests.
•	Smaller Angular framework download size: Doesn't require downloading the Angular compiler. Hence it dramatically reduces the application payload.
•	Detect template errors earlier: Detects and reports template binding errors during the build step itself
•	Better security: It compiles HTML templates and components into JavaScript. So there won't be any injection attacks.


The AOT compiler works in three phases,
•	Code Analysis: The compiler records a representation of the source
•	Code generation: It handles the interpretation as well as places restrictions on what it interprets.
•	Validation: In this phase, the Angular template compiler uses the TypeScript compiler to validate the binding expressions in templates.
How AOT works
The Angular AOT compiler extracts metadata to interpret the parts of the application that Angular is supposed to manage. 
You can specify the metadata explicitly in decorators such as @Component() and @Input(), or implicitly in the constructor declarations of the decorated classes. 
The metadata tells Angular how to construct instances of your application classes and interact with them at runtime.

The Angular compiler extracts the metadata once and generates a factory for TypicalComponent. When it needs to create a TypicalComponent instance, Angular calls the factory, which produces a new visual element, bound to a new instance of the component class with its injected dependency.

•	JIT(Just-in-Time) compilation
•	AOT(Ahead-of-Time) compilation

In JIT compilation, the application compiles inside the browser during runtime.
Whereas in the AOT compilation, the application compiles during the build time.


Top 5 Best Practices for Angular App 1Security
1.	Prevent cross-site scripting (XSS)
2.	Block HTTP-related vulnerabilities.
3.	Avoid risky Angular APIs.
4.	Don't customize Angular files.
5.	Stay updated with the latest Angular library.
6.	Use Route guards when required

How to prevent XSS?
XSS is a kind of injection attack.
XSS attacks occur when an attacker uses a web application to send malicious code, generally in the form of a browser side script, to a different end user.
You can enter below tag in textarea and access 
<script>alert(“XSS Attack");"</script>

For prevent use sanitizer like: 
<div [innerHTML]=’value’></div>

/* by style */
<div [style]=’value’></div>

/* by url */
<a [href]=’value’></a>
// or
<script [src]=’value’></script>

OR
We can use an angular build-in function called sanitization function like the bypassSecurityTrustHtml() function.

constructor(private sanitizer: DomSanitizer) {
}    

public sanitize(value: string) {
    return this.sanitizer.bypassSecurityTrustHtml(value);
}

What is angular animation?
•	Angular's animation system is built on CSS functionality in order to animate any property that the browser considers animatable. 
•	These properties includes positions, sizes, transforms, colors, borders etc. 
The Angular modules for animations are @angular/animations and @angular/platform-browser and these dependencies are automatically added to your project when you create a project using Angular CLI.

What are the steps to use animation module?
You need to follow below steps to implement animation in your angular project,
•	Enabling the animations module: Import BrowserAnimationsModule to add animation capabilities into your Angular root application module(for example, src/app/app.module.ts).

•	Importing animation functions into component files: Import required animation functions from @angular/animations in component files(for example, src/app/app.component.ts).
•	Adding the animation metadata property: add a metadata property called animations: within the @Component() decorator in component files(for example, src/app/app.component.ts)
What is Angular 1Ivy?
Angular Ivy is a rendering engine for Angular. 
Ivy Engine introduced several features and improvements related to decreasing bundle size and improving performance.
Angular 12 transitions away from View Engine (now deprecated). 
Protractor is no longer included in new Angular projects. 
Angular components will additionally now support inline Sass
What are the features included in ivy preview?
You can expect below features with Ivy preview,
1.	Smaller Bundle Sizes: Ivy generates smaller and more efficient JavaScript bundles, resulting in faster initial load times for your Angular applications. This is achieved through improved tree-shaking and dead code elimination.
2.	Faster Compilation: The Angular compiler in Ivy is faster, making development and build processes quicker. It uses incremental compilation, which means it only compiles changed parts of your application when you make code edits.
3.	Improved Debugging: Ivy provides better error messages and improved debugging capabilities, making it easier to identify and fix issues in your code.
4.	Localized Scope Checking: Ivy performs scope checking at the template level, which means that Angular can detect template binding issues more accurately and provide better error messages.
5.	Improved Ahead-of-Time (AOT) Compilation: Ivy enhances AOT compilation, resulting in faster startup performance for production-ready applications.
6.	Better Template Type Checking: Ivy enables stronger type checking for templates using TypeScript. This helps catch type-related errors at compile time, reducing runtime errors.
7.	Tree Shakable Services: With Ivy, services can be marked as “tree-shakable,” allowing you to include only the services your application actually uses in the final bundle.

What is 1lazy loading?
When the modules are loaded on demand, then it is called lazy loading.
•	Lazy loading is one of the most useful concepts of Angular Routing.
•	The main aim of lazy loading is to improve the performance of the Angular app by restricting the unnecessary loading of components.

Separate feature bundles
Load bundles on demand
Serve less code on first serve

const routes: Routes = [
  {
    path: 'customers',
    loadChildren: () => import('./customers/customers.module').then(module => module.CustomersModule)
  },
  {
    path: 'orders',
    loadChildren: () => import('./orders/orders.module').then(module => module.OrdersModule)
  },
  {
    path: '',
    redirectTo: '',
    pathMatch: 'full'
  }
];

How does one 1share data between components in Angular?
1. Parent to child using @1Input decorator

@Input is used to receive data in Angular,

 When passing data from Parent to Child component, you can use the @Input decorator in the Child component.

In the child component, we are using @Input decorator to capture data coming from a parent component and using it inside the child component’s template.

2. Child to parent using @Output and EventEmitter
@Output is used to send data outside.
When passing data from Child to Parent component, you can use the @Output decorator in the Child component.

In this method, we bind a DOM element inside the child component, to an event (click event for example) and using this event we emit data that will captured by the parent component:
  
As you can see in the child component, we have used @Output property to bind an EventEmitter. This event emitter emits data when the button in the template is clicked.

3. Child to parent using 1ViewChild decorator


In the above example, a property named “data” is passed from the child component to the parent component.
@ViewChild decorator is used to reference the child component as “child” property.
Using the ngAfterViewInit hook, we assign the child’s data property to the messageFromChild property and use it in the parent component’s template.
4. Unrelated Components: Sharing Data with a Service:
As we know multiple components share the common data and always need updated shared data. We use the BehaviorSubject to hold the data that we want to access throughout the application.
•	BehaviorSubject is both observer and type of observable.
•	BehaviorSubject always need an initial/default value.
•	Every observer on subscribe gets current value.
 I say type of observable because it is a little different to a standard observable. We subscribe to a BehaviourSubject just like we would a normal observable, but the benefit of a BehaviourSubject for our purposes is that:
•	It will always return a value, even if no data has been emitted from its stream yet
•	When you subscribe to it, it will immediately return the last value that was emitted immediately (or the initial value if no data has been emitted yet)
import {BehaviorSubject} from "rxjs/BehaviorSubject"
export class MyService {
    private state$ = new BehaviorSubject<any>('initialState');
    changeState(myChange) {
        this.state$.next(myChange);
    }
    getState() {
        return this.state$.asObservable();
    }
}

Explain the concept of 1Dependency Injection?
Dependency injection (DI), is an important application design pattern in which a class asks for dependencies from external sources rather than creating them itself. 
Dependencies in angular are nothing but services which have a functionality. Functionality of a service, can be needed by various components and directives in an application. Angular provides a smooth mechanism by which we can inject these dependencies in our components and directives.

So basically, we are just making dependencies which are injectable across all components of an application.

Angular comes with its own dependency injection framework for resolving dependencies(services or objects that a class needs to perform its function).
So you can have your services depend on other services throughout your application

Let’s understand how DI (Dependency Injection) works:

Consider the following service, which can be generated using:
ng g service test
    
      import { Injectable } from '@angular/core';

      @Injectable({
        providedIn: 'root'
      })
      export class TestService {
        importantValue:number = 42;

        constructor() { }

        returnImportantValue(){
          return this.importantValue;
        }
      }
    
  
As one can notice, we can create injectable dependencies by adding the @Injectable decorator to a class.

We inject the above dependency inside the following component:
    
      import { TestService } from './../test.service';
      import { Component, OnInit } from '@angular/core';

      @Component({
        selector: 'app-test',
        templateUrl: './test.component.html',
        styleUrls: ['./test.component.css']
      })
      export class TestComponent implements OnInit {
        value:number;
        constructor(private testService:TestService) { }

        ngOnInit() {
          this.value = this.testService.returnImportantValue();
        }
      }
    
  
One can see we have imported our TestService at the top of the page. Then, we have created an instance inside the constructor of the component and implemented the returnImportantValue function of the service.

From the above example, we can observe how angular provides a smooth way to inject dependencies in any component.

DI decouples components by removing the responsibility of creating and managing dependencies more flexible and modular architecture.


What is injector in angular?
The @Injectable() decorator marks it as a service that can be injected, but Angular can't actually inject it anywhere until you configure. 
An Angular dependency injector with a provider of that service. 
The injector is responsible for creating service instances and injecting them into classes
The Angular Injector is responsible instantiating the dependency and injecting into the component or service

What is Angular Material?
Angular Material is a collection of Material Design components for Angular framework following the Material Design spec. 
You can apply Material Design very easily using Angular Material. The installation can be done through npm or yarn,
npm install --save @angular/material @angular/cdk @angular/animations
(OR)
yarn add @angular/material @angular/cdk @angular/animations
It supports the most recent two versions of all major browsers. 
The latest version of Angular material is 18.1.1

Why does Angular need Node.js?
It is not mandatory to use node.js for developing angular application.
You can very well go ahead without node.js for developing angular application but it would not be wise to do so. 
Let me explain you some of the reasons how node.js makes angular app development process easier for us:
•	Node allows you to spin up a lightweight web server to host your application locally in your system.
•	NPM (Node Package Manager) comes with node.js by default. NPM allows you to manage your dependencies. So, you don’t have to worry for operations like adding a dependency, removing some, updating your package.json.
•	Third and the most important, npm gives you angular cli or ng cli(angular command line interface) . Angular CLI is a great tool for scaffolding your application. So, you don’t need to write boilerplates manually.
•	Angular recommends the use of TypeScript. Now, your browser does not understand TypeScript. It needs to be transpiled to JavaScript. Also, you need to bundle your js files and stylesheets together with the html doc so as to get the web app CLI which is ready to be hosted. Angular CLI helps you to do all these behind the scene. 
•	By default, ng cli uses webpack for bundling your application and is very helpful for beginners who have just jumped into web development with angular as it abstracts such complexities.
•	Angular does not need node.js directly. Node js is used for all the build and development tools. Angular is a framework and you may use typescript programming language to program us. 
•	Typescript is the most popular choice. A web browser such as Chrome, Firefox or Internet Explorer understands only Javascript so we have to transpile our Typescript to Javascript and for that we use typescript transpiler which requires NodeJS. 

What is 1trackBy?
Angular provides the trackBy feature which allows you to track elements when they are added or removed from the array for performance reasons.
The ngFor directive provides the trackBy function, which determines how Angular will track changes in objects inside a collection so that ngFor can perform efficient updates.

Angular 1Forms example
Template Driven Forms:
•	Template-driven forms are the basic forms that are suitable for the development of a limited number of fields and with simpler validation.
•	In this form, each field is represented as a property in the component class.
•	You Need to import FormsModule from the ‘@angular/forms’ package.

Following are the key concepts related to validation objects, directives, and properties that we used while creating the template-driven forms in Angular.

· ngForm Directive: This directive represents an angular form and exposes methods and properties related to it for validation and data manipulation purposes.

· ngModel Directive: This directive is used to achieve two-way data bindings between different form control elements.

· Validation Properties: Angular provides different validator properties that can be applied to form controls to indicate their validation state.
1. touched: A boolean indicating whether the control has been touched.
2. untouched: The opposite of touched
3. valid: A boolean indicating whether the control’s value is valid.
4. invalid: The opposite of valid

· Validation Directives: Angular provides several built-in validation directives that can be used with ngModel to perform validation. Some common ones include:
1. required: Ensures the control has a non-empty value.
2. min length and max length: Specifies the minimum and maximum length for the value.
3. pattern: Validates the value against a regular expression.
4. email: Validates that the value is a valid email address.

Reactive Forms Features

Reactive forms, or model-driven forms, are the types of forms in Angular that are suitable for creating a large form with different form fields and complex validation.
· In the reactive form, each form field is considered a Form Control, and a set of form controls is called a Form Group.
· The validation rules are defined in the component with the Validators object, and validation messages can be displayed in the template with the help of the validation property.
· ReactiveFormModule needs to be imported from the ‘@angular/forms’ package.
Below are some of the high-level differences between the two types:
1.	In template-driven forms you write validations inside the template(Declarative), while in reactive forms you can write the validation programmatically(Imperative) in the component. 
2.	Template-driven forms make use of the "FormsModule", while reactive forms are based on "ReactiveFormsModule".
3.	Template-driven forms are asynchronous in nature, whereas Reactive forms are mostly synchronous.
Both reactive and template-driven forms share underlying standard building blocks, which are the following.
•	FormControl: It tracks the value and validation status of the individual form control. 
•	FormGroup: It tracks the same values and status for the collection of form controls.  It defines a form with a fixed set of controls those can be managed together in an one object. It has same properties and methods similar to a FormControl instance. This FormGroup can be nested to create complex forms.
•	FormArray:It tracks the same values and status for the array of the form controls. It defines a dynamic form in an array format, where you can add and remove controls at run time. This is useful for dynamic forms when you don’t know how many controls will be present within the group.
•	ControlValueAccessor: It creates a bridge between Angular FormControl instances and native DOM elements.


What is FormBuilder in angular?

The FormBuilder provides shortens creating instances of a FormControl , FormGroup , or FormArray . It reduces the amount of boilerplate needed to build complex forms.

It is used to create a big reactive form with minimum code in Angular. FormBuilder has methods as group() , control() and array() that returns FormGroup , FormControl and FormArray respectively. Using FormBuilder we can directly pass object or array of object of a class to create the form.

What is a template reference variable and how would you use it in Angular ?
Template reference variables are basically used to create a reference to the input element that can be used later on in any template. 
It is also called the hashtag syntax # because it uses a hashtag to create a reference to an element in a template.

Example
                                                    
<input #mobile placeholder="mobile number">

Here a reference has been created to get the value of the input like:

//mobile is the input element

<button (click)="callmobile(mobile.value)">Call</button>

The above example is a foolproof method to avoid using the ngModel or some type of data binding by a simple form not requiring much validation.

What is 1NgRx?
NgRx stands for Angular Reactive Extensions
NgRx is a state management system that is based on the 1Redux pattern
NgRx uses concepts such as actions, reducers, effects, and selectors to manipulate the state in a controlled manner.

1State
•	@ngrx/store: A Redux-based state management library for Angular. It is the only library required to work with NgRx.
•	@ngrx/effects: It helps us handle side effects in the @ngrx/store.
•	@ngrx/router-store: It connects our Angular router to the @ngrx/store.
•	@ngrx/entity: It helps us manage entity collections.
•	@ngrx/component-store: It helps us manage local states in our Angular components.
What is safe navigation operator(elvis)?
The safe navigation operator(?)(or known as Elvis Operator/Chaining Operator) is used to guard against null and undefined values in property paths when you are not aware whether a path exists or not. i.e. It returns value of the object path if it exists, else it returns the null value.
For example, you can access nested properties of a user profile easily without null reference errors as below,
<p>The user firstName is: {{user?.fullName.firstName}}</p>
Using this safe navigation operator, Angular framework stops evaluating the expression when it hits the first null value and renders the view without any errors.
The Safe navigation operator can be used to prevent errors while trying to access the object properties of non-existent objects.
Here’s an example explaining the above statement:
{{ phone?.number }}
This above line of code only evaluates the number when the phone is not null or undefined. This is very suitable in situations where a phone is something that is loading asynchronously.
Angular 1Unit testing?
Angular Unit testing is the process of testing small and isolated pieces of code (modules) in your Angular application. 
This provides an added advantage to the users as they can add any new features without breaking any other part of their application.
In Angular 16 and above version Karma has deprecated, now for unit test cases you can use jest
npm I jest jest-preset-angular@types/jest -D
Jasmine and Karma frameworks are used for Unit Testing of the Angular applications.
Jasmine is a free and open-source Behavior Driven Development (BDD) framework. It can run on any JavaScript-enabled platform. 
Karma is a task runner for our tests. It allows the users to execute their Jasmine test codes in multiple real-time browsers from the command line. 

How to write a Unit Test in Angular?
There are three main methods in this test file:
•	describe() – It’s a suite of Test scripts that calls a global Jasmine function with two parameters: a string and a function. It also consists of beforeEach block.
•	it() – It’s the smallest unit test case that is written to be executed, which calls a global Jasmine function with two parameters: a string and a function. Multiple it() statements can be written inside the describe()
•	expect() – Every it() statement has a expect() function which takes a value and expects a return in true form
spyOn Jasmin method – 
Stub – A dummy piece of code that lets the test run, but you don’t care what happens to it.
Mock – a dummy piece of code, that you verify is called correctly as part of the test.
Spy - a dummy piece of code, that intercepts some calls to real piece of code, allowing you to verify call without replacing the entire original array.
Spy is a feature of Jasmine that allows you to take a control of class, function, or object and modify the behavior in such a way as you want. 
The Angular testing package includes two utilities called TestBed and async. 
TestBed is the main utility package. (Please see the app.component.spec.ts file below)
Run by below command-
ng test
ng test --code-coverage --watch

npm start and ng serve difference?

npm start will run whatever you have defined for the start command of the scripts object in your package.json file.
So if it looks like this:
"scripts": {
  "start": "ng serve"
}

Then npm start will run ng serve.

1Performance of your Angular App:

1.	Enabling production mode(Tree shaking)
2.	AOT
3.	Minification
4.	Avoiding function calls and getters in views
5.	Pure pipes
6.	Lazy loading modules
7.	Code splitting
8.	Avoid using ngIf with complex expressions
9.	OnPush change detection(ChangeDetectionStrategy)
10.	Async pipe
11.	ngDoCheck
12.	Track by function
13.	Zone.js
14.	Unsubscribing observables
15.	Optimize your images
16.	Web workers

What are 1Web 1Workers?
•	Web Workers is a code of JavaScript which runs in the background, independently of other scripts, without disturbing the performance of the page. 
•	It is used for computing-heavy tasks like an access database or function.

1Interfaces
•	An interface is a way to define a contract on a function with respect to the arguments and their type. 
•	Along with functions, an interface can also be used with a Class as well to define custom types.
•	An interface is an abstract type, it does not contain any code as a class does. 
•	It only defines the 'signature' or shape of an API.
 During transpilation, an interface will not generate any code, it is only used by Typescript for type checking during development.

What is 1Transpiling in Angular?
Transpilling means converting TypeScript into JavaScript. 
You can write the code for your Angular application in TypeScript (or another language such as Dart) that is then transpiled to JavaScript for the application. 
This happens internally and automatically.


Angular 1Change Detection:
Change Detection means updating the DOM whenever data is changed. 
Angular provides two strategies for Change Detection.
In its default strategy, whenever any data is changed, Angular will run the change detector to update the DOM. 
In the onPush strategy, Angular will only run the change detector when a new reference is passed to @Input() data.
the changeDetection property of the @Component decorator to ChangeDetectionStrategy.OnPush as shown in listing below:
import { Component, Input, ChangeDetectionStrategy } from '@angular/core';
@Component({
    selector: 'app-message',
    changeDetection: ChangeDetectionStrategy.OnPush,
    template: `
    <h2>
    Hey {{person.firstname}} {{person.lastname}} !
    </h2>
    `
})
export class MessageComponent {
    @Input() person;
}

With onPush, Angular will only depend on the component’s inputs, events, markForCheck method, or the use of the async pipe in the template, to perform a change detection mechanism and update the view.
What are the ways to trigger change detection in Angular?
You can inject either ApplicationRef or NgZone, or ChangeDetectorRef into your component and apply below specific methods to trigger change detection in Angular. i.e, There are 3 possible ways,
i.	ApplicationRef.tick(): Invoke this method to explicitly process change detection and its side-effects. It check the full component tree.
ii.	NgZone.run(callback): It evaluate the callback function inside the Angular zone.
iii.	ChangeDetectorRef.detectChanges(): It detects only the components and it's children.

What is the rest parameter and spread operator?
Both represented by three dots (…)
Both rest parameter and spread operator were introduced in the ES6 version of javascript.

1Rest Parameter/Operator ( … ):
•	In functions when we require to pass arguments but were not sure how many we have to pass that time we use rest parameter
•	Any number of arguments will be converted into an array using the rest parameter.
•	Rest parameters can be used by applying three dots (...) before the parameters.
function extractingArgs(...args){
  return args[1];
}

// extractingArgs(8,9,1); // Returns 9

function addAllArgs(...args){
  let sumOfArgs = 0;
  let i = 0;
  while(i < args.length){
    sumOfArgs += args[i];
    i++;
  }
  return sumOfArgs;
}

addAllArgs(6, 5, 7, 99); // Returns 117
addAllArgs(1, 3, 4); // Returns 8

function abc(a, ...rest) {
return rest;
}
console.log(abc(10, 1, 2, 3, 4, 5));
**Note- Rest parameter should always be used at the last parameter of a function.
// Incorrect way to use rest parameter
function randomFunc(a,...args,c){
//Do something
}

// Correct way to use rest parameter
function randomFunc2(a,b,...args){
//Do something
}

1Spread operator (…): 
It works by taking all the items in an array and spreading them out, essentially unpacking the array so that each item becomes an individual element.
It’s like taking a bunch of items from a box and laying them out separately on a table.
In TypeScript, the spread operator (in form of ellipsis) can be used to initialize arrays/objects from another array/object.
The spread operator is a useful and quick syntax for adding items, combining, and spreading out an array/object into a function’s arguments.
Initialize arrays another array
let origArrayOne = [ 1, 2, 3];                          //1,2,3
let origArrayTwo = [ 4, 5, 6];                          //4,5,6
 
//Create new array from existing array
let copyArray = [...origArrayOne];                      //1,2,3
 
//Create new array from existing array + more elements
let newArray = [...origArrayOne, 7, 8];             //1,2,3,7,8 
 
//Create array by merging two arrays
let mergedArray = [...origArrayOne, ...origArrayTwo];   //1,2,3,4,5,6

function abc(a, b, c) {
return a + b + c;
}
console.log(abc(...[1, 2, 3]))
Advantages:
•	Arrow functions reduce the size of the code.
•	This makes it easier to work with the individual items rather than dealing with the entire array as a single entity
•	The return statement and function brackets are optional for single-line functions.
•	It increases the readability of the code.

function addFourNumbers(num1,num2,num3,num4){
  return num1 + num2 + num3 + num4;
}

let fourNumbers = [5, 6, 7, 8];


addFourNumbers(...fourNumbers);
// Spreads [5,6,7,8] as 5,6,7,8

let array1 = [3, 4, 5, 6];
let clonedArray1 = [...array1];
// Spreads the array into 3,4,5,6
console.log(clonedArray1); // Outputs [3,4,5,6]


let obj1 = {x:'Hello', y:'Bye'};
let clonedObj1 = {...obj1}; // Spreads and clones obj1
console.log(obj1);

let obj2 = {z:'Yes', a:'No'};
let mergedObj = {...obj1, ...obj2}; // Spreads both the objects and merges it
console.log(mergedObj);
// Outputs {x:'Hello', y:'Bye',z:'Yes',a:'No'};
***Note- Key differences between rest parameter and spread operator:
•	Rest parameter is used to take a variable number of arguments and turns them into an array while the spread operator takes an array or an object and spreads it
•	Rest parameter is used in function declaration whereas the spread operator is used in function calls
•	The main difference between the two operators lies in their names. The spread operator in JavaScript expands values in arrays and strings into individual elements whereas, the rest operator, puts the values of user-specified data into a JavaScript array.
Note: There must be only one rest parameter in javascript functions.
Note: There can be more than one spread operator in javascript functions.
The rest operator is used to put the rest of some specific user-supplied values into a JavaScript array
The spread operator (...) helps you expand iterables into individual elements.
The spread syntax works within array literals, function calls, and initialized property objects to spread the values of iterable objects into separate items. So effectively, it does the opposite thing from the rest operator.

Why and When Use Ng-template, 1NgContent, and 1NgContainer in Angular?
•	ng-template help to define a template that can be reused multiple times within an Angular component.
•	ng-container when we need to group elements without adding additional nodes to the DOM. One common use case for ng-container is to apply a structural directive(*ngFor) to multiple elements without wrapping them in an additional HTML tag
•	ng-content is used to render content dynamically that is passed in from the parent component

// my-box.component.ts
@Component({
  selector: 'my-box',
  template: `
    <div class="box">
      <div class="header">
        <ng-content select="[header]"></ng-content>
      </div>
      <div class="content">
        <ng-content></ng-content>
      </div>
    </div>
  `,
  styles: [
    `
      .box {
        border: 1px solid black;
        padding: 10px;
      }
      .header {
        font-weight: bold;
      }
    `
  ]
})
export class MyBoxComponent {}

// parent.component.html
<my-box>
  <div header>Header content</div>
  <p>Box content</p>
</my-box>

1Routing:
•	To handle the navigation from one view to the next, you use the Angular Router.
•	Routing helps you to define the navigation for your angular application.
What is router 1outlet?
The RouterOutlet is a directive from the router library and it acts as a placeholder that marks the spot in the template where the router should display the components for that outlet. Router outlet is used like a component,
<router-outlet></router-outlet>

What are router links?
•	The RouterLink is a directive on the anchor tags give the router control over those elements. 
•	Routerlink simply helps in navigation but doesn’t directly involve itself with guards or authentication.
Since the navigation paths are fixed, you can assign string values to router-link directive as below,
<h1>Angular Router</h1>
<nav>
  <a routerLink="/todosList" >List of todos</a>
  <a routerLink="/completed" >Completed todos</a>
    <a routerLink="/todosList" routerLinkActive="active">List of todos</a>
  <a routerLink="/completed" routerLinkActive="active">Completed todos</a>
</nav>
<router-outlet></router-outlet>

Query Parameters: 
Using Query Parameters with Router.navigate
Query parameters in Angular allow for passing optional parameters across any route in the application.
Query parameters are different from regular route parameters, which are only available on one route and are not optional
goProducts() {
  this.router.navigate(
    ['/products'],
    { queryParams: { order: 'popular' } }
  );
}
Get params we need subscribe.
constructor(private route: ActivatedRoute) { }
  ngOnInit() {
    this.route.queryParams
      .filter(params => params.order)
      .subscribe(params => {
        console.log(params); // { order: "popular" }
        this.order = params.order;
        console.log(this.order); // popular
      }
    );
  }

1Authentication vs Authorization?
•	Authentication means confirming your own identity, whereas authorization means being allowed access to the module. 
Angular 1Auth 1Guard?
•	The auth guard is an angular route guard that's used to prevent unauthorized users from accessing restricted routes.
•	When a user is navigating to a specific route in the application, the Auth Guard can check whether the user is authenticated and authorized to access that particular route.
•	It will manage different access levels between authenticated and non-authenticated users.
•	If the user is authenticated, the Auth Guard allows the navigation to proceed further. Otherwise, it will redirect the user to a login page or another appropriate route, preventing access to the protected content.
To implement authentication and authorization in this scenario, you can follow these steps:
•	Create a login component that accepts user credentials and sends them to a login service for authentication.
•	Create an authentication service that verifies user credentials and sets an authentication token or session cookie.
•	Create an authorization service that checks user roles and permissions and grants access to specific features.
•	Use route guards to restrict access to specific pages or features based on user roles and permissions using canActivate() method.
•	Use the HttpClient service to make API requests that require authentication and authorization.
•	Use the HttpInterceptor interface to add authorization headers to outgoing API requests.
Here are some additional tips for implementing authentication and authorization in Angular:
•	Use the localStorage or sessionStorage objects to store authentication tokens or session cookies.
•	Use JSON Web Tokens (JWT) for secure authentication and authorization.
•	Implement hashed password or encryption to protect user passwords and sensitive data.
•	Use role-based access control (RBAC) or attribute-based access control (ABAC) to define user roles and permissions.
5 different types of Route Guards in Angular:
•	CanActivate: Controls if a route can be activated.
•	CanActivateChild: Controls if children of a route can be activated.
•	CanLoad: Controls if a route can even be loaded. This becomes useful for feature modules that are lazy loaded. They won’t even load if the guard returns false.
•	CanDeactivate: Controls if the user can leave a route. Note that this guard doesn’t prevent the user from closing the browser tab or navigating to a different address. It only prevents actions from within the application itself.
•	Resolve: While not technically guard, it’s often used in conjunction with guards. Resolve is a feature that pre-fetches data before a route is activated, ensuring that the route has all the necessary data before rendering.
How would you handle authentication and authorization in an Angular Application?
1.	Use a token-based authentication system to authenticate users and maintain user sessions.
2.	Use Angular’s HTTP Interceptor to automatically attach authentication headers to requests. 
3.	Use Angular’s Route Guards to control access to specific routes and feature based on user roles and permissions.
4.	Store user authentication and authorization data in a secure cookie or local storage
5.	Use server-side authorization check to ensure that user have the necessary permissions to perform specific actions.
  
const routes: Routes = [
  {path: '', component:ProductListComponent, pathMatch:'full', canActivate: [AuthGuard]},
  {path: 'login', component:LoginComponent},
  {path: 'products', component:ProductListComponent, canActivate: [AuthGuard]},
  {path: 'products', component:ProductListComponent, canActivate: [AuthGuard]},
  {
    path: 'product/:id', component: ProudctDetailsComponent,
canActivateChild: [AuthGuard],
    children: [
      { path: 'rating', component: ProudctRatingComponent, canDeactivate: [AuthGuard] },
      { path: 'offers', component: ProudctOffersComponent }
    ]
  },
  {
    path: 'service',
    loadChildren: () => import('./modules/product-service/product-service.module').then(m => m.ProductServiceModule),
    canLoad: [AuthGuard]
  },
  {path: '**', component:ProductListComponent, pathMatch:'full', canActivate: [AuthGuard]}
];

What is SSR?
Server side rendering (SSR) is a process that involves rendering pages on the server, resulting in initial HTML content which contains initial page state. Once the HTML content is delivered to a browser, Angular initializes the application and utilizes the data contained within the HTML.
The main advantages of SSR as compared to client-side rendering (CSR) are:
•	Improved performance: SSR can improve the performance of web applications by delivering fully rendered HTML to the client, which the browser can parse and display even before it downloads the application JavaScript. This can be especially beneficial for users on low-bandwidth connections or mobile devices.
•	Better SEO: SSR can improve the search engine optimization (SEO) of web applications by making it easier for search engines to crawl and index the content of the application.
Note: In Angular v17 and later, server.ts is no longer used by ng serve. The dev server will use main.server.ts directly to perfom server side rendering.

How to handle 1large volume / huge data of records? 
•	Virtual scrolling
import { ScrollingModule } from '@angular/cdk/scrolling';
<cdk-virtual-scroll-viewport itemSize="50"> 
<div *cdkVirtualFor="let item of items">
{{ item }}
</div>
</cdk-virtual-scroll-viewport>
•	Pagination
•	Manual rendering
o	Use Track by in ngFor to improve rendering performance by providing a unique identifier for each item
o	Use ChangeDetectionStrategy.onPush to reduce change detection cycle for components
•	Infinite scrolling
•	Lazy loading
•	Data optimization

Angular Authentication with 1JWT
JSON Web Tokens (JWTs). 
Your Angular app can talk to a backend that produces a token.
The Angular app can then pass that token in an Authorization header to the backend to prove they're authenticated. 
The backend should verify the JWT and grant access based on its validity.

How do JWT tokens work?
1.	Displays a login form, and sends user credentials to the back-end service to get user’s claims, a JWT access token, and a refresh token.
2.	Stores the JWT access token and refresh token in a browser’s localStorage, so that the application in different browser tabs can use the same tokens.
3.	Adds an authorization header when sending HTTP requests.
4.	Tracks the expiration time of the access token and sends a request to refresh tokens when the access token is about to expire.
5.	Removes the tokens from localStorage when the user logs out.

Explain The Key Differences Between 1LocalStorage And 1SessionStorage Objects.
Both localStorage and sessionStorage are part of web API which are used to store ‘KEY’ — ‘VALUE’ pairs in Angular. Generally browsers provides around 10 MB of storage space

•	The localStorage object stores the data without an expiry date. However, sessionStorage object stores the data for only one session.
•	LocalStorage object, data will not delete when the browser window closes. However, In sessionStorage case, the data gets deleted if the browser window closes.
•	The data in the localStorage can be shared between multiple windows of the browser but the data in sessionStorage is accessible only in the current window of the browser also each tab operates within its own isolated session, and the storage is not shared between them.

localStorage.setItem(‘name’,’Nixon’); // name is a key and nexon is a value
let name = localStorage.getItem(‘name’);
localStorage.removeItem(‘name’);
localStorage.clear();
// Create item:
let myObj = { name: 'Nixon', profession: 'Developer' };
localStorage.setItem(key, JSON.stringify(myObj));// Read item:
let item = JSON.parse(localStorage.getItem(key));

Which type of data sent to the server from client side in request?
When a client sends a request to a server, it typically includes various types of data depending on the nature of the request. The most common types of data sent from the client side in a request include:

•	URL Parameters: Data is often appended to the URL as query parameters. For example
•	HTTP Headers: Headers provide additional information about the request. Common headers include Content-Type (indicating the type of data in the request body) and Authorization (providing authentication credentials).
•	Request Body: The request body carries the main data for the request. The format of the data depends on the HTTP method and the Content-Type header. Common formats include:
JSON: Used with application/json content type.
Form Data: Used with application/x-www-form-urlencoded or multipart/form-data content types.
Text: Used with text/plain content type.
XML: Used with application/xml content type.
•	Cookies: If the client has cookies related to the domain, they are automatically sent with the request. Cookies often contain session information or other data.
•	HTTP Method: The HTTP method (e.g., GET, POST, PUT, DELETE) itself is a piece of information sent from the client, indicating the type of operation to be performed on the server.
•	Path Parameters: In RESTful APIs, path parameters are part of the URL path itself.
•	User-Agent: The User-Agent header provides information about the client application making the request. It can include details about the browser or the client-side application.
•	Other Custom Headers: Clients may include additional custom headers based on the requirements of the server or the application.

How to create Angular 1Library?
Let us create a workspace for our library!
ng new <application-name> --create-application=false
ng generate library <library-name>
Add a build library script in your root package.json as:
"build-library": "ng build nishu-library”
For publish library do the following command
Npm publish –access public
You need to logedIn NPM website.

What is the use of angular cdk?
The Angular Component Dev Kit (CDK) is a library of predefined behaviors included in Angular Material, a UI component library for Angular developers. 
It contains reusable logic for many features that are used as common building blocks for the interfaces of Angular applications.

How To Use Internationalization (i18n) or localization in Angular 

Internationalization is the process of supporting multiple languages in your applications.
This can be accomplished in an Angular application through third party libraries, such as ngx-translate, or you can use the built-in i18n functionality.

What is 1Zone?
A Zone is an execution context that persists across async tasks. 
Angular relies on zone.js to run Agular’s change detection processes when native JavaScript operations raise events
What is NgZone?
Angular provides a service called NgZone which creates a zone named angular to automatically trigger change detection when the following conditions are satisfied.
i.	When a sync or async function is executed.
ii.	When there is no microTask scheduled.
What are the methods of NgZone used to control change detection?
NgZone service provides a run() method that allows you to execute a function inside the angular zone. 
This function is used to execute third party APIs which are not handled by Zone and trigger change detection automatically at the correct time.

export class AppComponent implements OnInit {
  constructor(private ngZone: NgZone) {}
  ngOnInit() {
    // use ngZone.run() to make the asynchronous operation in the angular zone
    this.ngZone.run(() => {
      someNewAsyncAPI(() => {
        // update the data of the component
      });
    });
  }
}

Whereas runOutsideAngular() method is used when you don't want to trigger change detection. 
Use this method when you know no data will be updated


Difference between 1dependencies, 1devDependencies and peerDependencies
Dependencies:
— The `dependencies` property is used to list the packages that are required for the project to run in a production or deployment environment.
— These packages are necessary for the application’s core functionality and are typically required at runtime.
— When you install the project dependencies using `npm install`, the packages listed in the `dependencies` section are installed.
Syntax:
npm install <package name>
Dev Dependencies:
— The `devDependencies` property is used to list the packages that are only required during development, such as testing frameworks, build tools, and development-specific utilities.
— These packages are not necessary for the application to run in a production environment but are helpful during development and testing phases.
— When you install the project dependencies along with dev dependencies using `npm install`, the packages listed in both the `dependencies` and `devDependencies` sections are installed.
Use the below command to add more dev Dependencies in your project:
npm install <package name> --save-dev
Peer Dependencies:
In package.json file, there is an object called as peerDependencies and it consists of all the packages that are exactly required in the project or to the person who is downloading and the version numbers should also be the same. That is the reason they were named as peerDependencies. The best example is ‘react’ which is common in every project to run similarly. 
Note: These dependencies are not automatically installed. npm gives a warning message whenever there is a peer Dependency and these are different dependencies compared to the above-discussed dependencies.

Can I share services using modules?
No, it is not recommended to share services by importing module. i.e Import modules when you want to use directives, pipes, and components only. The best approach to get a hold of shared services is through 'Angular dependency injection' because importing a module will result in a new service instance.
What is a service worker and its role in Angular?
Service workers are this wonderful new web platform feature that lights up some great functionality like URL response caching. This caching is the magic that enables progressive web applications to work offline.
A service worker is a script that runs in the web browser and manages caching for an application.
Adding a service worker to an Angular application is one of the steps for turning an application into a Progressive Web App (also known as a PWA).
 Service workers function as a network proxy.
This newer caching system replaces a previous attempt at powering offline web experiences called appCache
Starting from 5.0.0 version, Angular ships with a service worker implementation. Angular service worker is designed to optimize the end user experience of using an application over a slow or unreliable network connection, while also minimizing the risks of serving outdated content.
1Progressive Web Apps for Angular: 1pwa
Progressive Web Apps is a name given to a set of new W3C standards.
It allow any web application to feel and behave very much like a native app on a mobile device:
•	Offline caching with service workers so your app can work without an internet connection
•	Application manifest to define the look and feel of your app (splash screen, icons, name, full screen or not)
•	Install to home screen feature so your web app can be accessed just like any other native app
•	Web notifications so you can send background notifications to the user, just like native mobile apps do!

What are the design goals of service workers?
Below are the list of design goals of Angular's service workers,
i.	It caches an application just like installing a native application
ii.	A running application continues to run with the same version of all files without any incompatible files
iii.	When you refresh the application, it loads the latest fully cached version
iv.	When changes are published then it immediately updates in the background
v.	Service workers saves the bandwidth by downloading the resources only when they changed.

What is 1Linting
•	Linting is the process of running a program that analyses your code for programmatic and stylistic errors. 
•	A Linting tool, or a linter, checks any potential errors in your code such as syntax errors, incorrectly spelled variable names, and many more. 
•	This can save time and help you write better code.

What is transition function?
•	The animation transition function is used to specify the changes that occur between one state and another over a period of time. 
•	It accepts two arguments: the first argument accepts an expression that defines the direction between two transition states, and the second argument accepts an animate() function.
Let's take an example state transition from open to closed with an half second transition between states.
transition('open => closed', [
  animate('500ms')
]),

What is codelyzer?
•	Codelyzer provides set of tslint rules for static code analysis of Angular TypeScript projects. 
•	You can run the static code analyzer over web apps, NativeScript, Ionic etc. Angular CLI has support for this and it can be use as below,
ng new codelyzer
ng lint

How angular get load and 1start / 1work?
1.	Every Angular app consists of a file named angular.json. This file will contain all the configurations of the app. While building the app, the builder looks at this file to find the entry point of the application.
2.	Inside the build section, the main property of the options object defines the entry point of the application which in this case is main.ts.
3.	The main.ts file creates a browser environment for the application to run, and, along with this, it also calls a function called bootstrapModule, which bootstraps the application.
4.	The AppModule is declared in the app.module.ts file. This module contains declarations of all the components.
5.	In the file AppComponent is getting bootstrapped. This component is defined in app.component.ts file. This file interacts with the webpage and serves data to it.
6.	After this, Angular calls the index.html file. This file consequently calls the root component that is app-root. The root component is defined in app.component.ts. 


main.ts  >>   app.Module.ts  >>  app.component.ts  >>  index.html  >>  app.component.html  


What is a 1bootstrapping module?
•	Every application has at least one Angular module
•	The root module that you bootstrap to launch the application is called as bootstrapping module. It is commonly known as AppModule. 
•	The default structure of AppModule generated by AngularCLI

How to do 1bootstrap application?

•	Inside the build section, the main property of the options object defines the entry point of the application which in this case is main.ts.
•	The main.ts file creates a browser environment for the application to run, and, along with this, it also calls a function called bootstrapModule, which bootstraps the application. These two steps are performed in the following order inside the main.ts file:

import { platformBrowserDynamic } from '@angular/platform-browser-dynamic';
platformBrowserDynamic().bootstrapModule(AppModule)

In the above line of code, AppModule is getting bootstrapped.

Angular 1new 1features: Latest version is 18
Most prominent features of Angular 15:
•	Stable Standalone APIs
Now Angular 15 can allow developers to build Angular applications without any module
Components, directives, and pipes can now be marked as standalone: true
Existing applications can optionally and incrementally adopt the new standalone style without any breaking changes
The standalone flag and component imports
@Component({
  standalone: true,
  selector: 'photo-gallery',
  imports: [ImageGridComponent],
  template: `
    ... <image-grid [images]="imageList"></image-grid>
  `,
})
export class PhotoGalleryComponent {
  // component logic
}

•	Forms
The forms package now includes the utility functions like, isFormControl, isFormGroup, isFormRecord, and isFormArray.
Most prominent features of Angular 16:
•	Angular 1Signals
Signals are reactive in nature and has this producer-consumer design. 
Angular signals wrap around a value (holds a value) and then notifies the user of any changes. A signal’s value is always read through a getter function
There are two types of signals: Writable Signals and Computed Signals


import { Component, signal } from ‘@angular/core’;

@Component({
selector: ‘app-signal-example’,
template: `
<div>
<p>Current Value: {{ mySignalValue() }}</p>
<button (click)=”setNewValue()”>Set New Value</button>
<button (click)=”updateValue()”>Update Value</button>
</div>
`,
})

export class SignalExampleComponent {
mySignal = signal({ foo: ‘bar’ });
setNewValue() {
this.mySignal.set({ foo: ‘bar1’ });
}
updateValue() {
const currentValue = this.mySignal();
this.mySignal.set({ …currentValue, foo: currentValue.foo + ‘1’ });
}
}
•	Required Component Inputs
•	esbuild-Based Build System
•	Standalone Project Support
•	Self-closing tags
Most prominent features of Angular 17:
Starting with Angular version 14, they introduced standalone components, allowing users to build applications without the need for modules. By version 17, standalone components became the default in our applications.
Now you will have 
// app.config.ts

•	New Syntax for Control Flow in Templates:
The new control flow syntax is based on the @- syntax, which is similar to the syntax used in other programming languages like JavaScript and Python.
@for, @if, @else, @else if and @switch have upended the traditional @nglf, @ngfor.
This new construct makes the code structure simpler, clearer, and more expressive—while eliminating the need of using extra tags or the ng-template tag.
@for (product of products(); track product.id) {
    <div class="card">
        <h2 class="card-title">{{product.productName}}</h2>
        […]
    </div>
    }
@empty {
    <p class="text-lg">No Products found!</p>
}

@Component({
  standalone: true,
  selector: 'app-root',
  template: `
    @if(name === 'SFEIR'){
      <ul>
         @for(entity of entities; track entity.id) {
           <li>{{ entity.name }}</li>
         }@empty {
           No data
         }
      </ul>
    }@else {
      Name not correct
    }
  `
})
export class AppComponent {
  name = 'SFEIR';
  entities = [{ name: 'Luxembourg', id: 'LU' }];
}
•	Improved Build Performance with ESBuild:
"builder" : "@angular-devkit/build-angular:browser-esbuild"
•	Deferred Loading:
Probably one of the most important features of this release. The ability to lazyload our components easily.
It is making easy to lazyload our components by taking into account all the stages of lazyloading.

On the other hand, you will be able to use the following triggers within the defer blocks:
on idle: This trigger condition is met when the browser state becomes idle. It is commonly used to defer loading until the browser is not busy with other tasks.
on viewport: This trigger condition is met when the deferred content comes into the viewport, meaning it becomes visible to the user. It is useful for lazy loading content that is below the fold or not immediately visible.
on interaction: This trigger condition is met when the user interacts with the placeholder or the surrounding elements. It is useful when you want to load the deferred content upon user interaction, such as clicking or hovering.
on hover: This trigger condition is met when the user hovers over the placeholder or the surrounding elements. It is useful for lazy loading content that should be loaded when the user hovers over it.
on immediate: This trigger condition is met immediately, without any delay. It is useful for situations where you want to load the deferred content immediately without waiting.
on timer: This trigger condition is met after a specified delay. It allows you to set a timer and load the deferred content after the specified time.

Most prominent features of Angular 18:
•	Zoneless Applications:
Developers can now explore this new zoneless support by adding provideExperimentalZonelessChangeDetection to their application bootstrap process and eliminating zone.js from polyfills in angular.json.
bootstrapApplication(App, {
providers: [
provideExperimentalZonelessChangeDetection()
]
});
•	Default content in ng-content
•	Latest ng-template API
•	Material 3, signals, deferable views, and built-in control flow from version 17 are now stable in version 18
•	Routing: redirect as a function:
You used the redirectTo property. This property took as its value only a character string
It is now possible to pass a function with this property
•	New Official Documentation Website:
Angular developers now have a new home at Angular with angular.dev being declared as the official documentation website. So, from now onwards all the requests to angular.io will be automatically forwarded to angular.dev.

Explain 1MVVM architecture
MVVM architecture consists of three parts:

1. Model 
2. View 
3. ViewModel

Model In simple terms it contains data of an object. The Model is represented by services or classes responsible for data management.

View: This will be the HTML template of a component which serve as the View, displaying data and capturing user input.

ViewModel 
A viewmodel handles the logic of the application. 
It manages the data of a model and displays it in the view.
In Angular, the ViewModel is often represented by Components and associated TypeScript classes. 
The Component class contains the application logic and interacts with services to retrieve and manipulate data.
Any change in the view, the viewmodel takes a note and changes the appropriate data inside the model.
View and ViewModel are connected with data-binding (two-way data-binding in this case). 
An abstraction layer is an API (set of functions) which is hiding the underlying implementation/complexity

What is 1MVC Architecture?
1.	Model – It is responsible for managing application data. It responds to the requests from view and to the instructions from the controller to update itself.
2.	View – It is responsible for displaying all data or only a portion of data to the users. It also specifies the data in a particular format triggered by the controller’s decision to present the data. They are script-based template systems such as JSP, ASP, PHP and very easy to integrate with AJAX technology.
3.	Controller – It is responsible to control the relation between models and views. It responds to user input and performs interactions on the data model objects. The controller receives input, validates it, and then performs business operations that modify the state of the data model

What is MVC and MVVM?
MVC (Model-View-Controller) and MVVM (Model-View-ViewModel) are architectural design patterns used in iOS app development. MVC separates an app into three components: model, view, and controller, while MVVM adds a ViewModel layer between the view and the model.
What are the main differences between MVC and MVVM?
In MVC, the controller handles user input and updates the view accordingly, while in MVVM, the ViewModel acts as a mediator between the view and the model, managing data binding and providing a clean separation of concerns.

MVVM enhances testability and allows for better code reusability. It promotes a more declarative approach to UI development and enables easier integration of reactive programming frameworks.
MVC is a good choice for small to medium-sized projects with straightforward requirements.
MVVM is beneficial for larger projects that require more extensive data binding and event-driven interactions.
Communication
In MVC, the View communicates directly with the Controller to handle user interactions and updates. The Controller then interacts with the Model to retrieve or update data. The View does not directly reference the Model.  
In MVVM, the View communicates with the ViewModel through data binding. The ViewModel exposes properties and commands that the View binds to. The ViewModel, in turn, interacts with the Model to retrieve or update. 

Can I mix elements of MVC and MVVM?
Yes, it is possible to mix elements of both patterns. You can incorporate MVVM concepts within an existing MVC architecture by introducing a ViewModel layer to handle data binding and separation of concerns.

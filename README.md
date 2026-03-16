# everest-climb
What is 1Angular?
•	Angular is an open-source web application framework that is typescript based.
•	It is one of the most popular JavaScript frameworks that is mainly maintained by Google. 
•	It offers an easy to use and powerful way of building front end web-based applications.
•	Angular provides a set of ready-to-use modules that simplify the development.

Name some common or popular Angular features. 
•	Templates
•	Dependency Injection (DI)
•	Directive
•	Code splitting
•	Child-Parent Relationship
•	Data Binding
•	Localization
•	Validation
•	Testing
•	Component-based architecture – applications are written as a set of independent components.
•	Parts can be created, tested, integrated using Angular CLI.
•	Great support for complex animations without writing much code.
•	Because of the component router, Angular supports automatic code-splitting. Hence only the code required to render a particular view is loaded.
•	Cross-platform application development.

Differentiate between Angular and 1AngularJS.

Why do people use Angular? 
•	Great support by Google, thus making the platform user-friendly and trustworthy.
•	A component-based architecture where the application is divided into functional and logical components that are independent of each other. 
•	Parts can be decoupled, replaced, or reused easily. This type of architecture also ensures easier testing at each stage.
•	A lot of reusable code and third-party components are available, thus improving productivity.
•	The code is rendered faster because it gets converted from TypeScript (or HTML) to JavaScript during the build process itself. This is called the Ahead-of-Time (AOT) compilation.
•	Command Line Interface (CLI) – CLI facilitates development in the most efficient way. You can create a new project, add your functionalities, and test them quickly. Further, initialization and configuration become easy too.
•	Excellent documentation and support community.
•	Ability to add a custom directive
•	Exceptional community support
•	Facilitates client and server communication
•	Features strong features, such as Animation and Event Handlers
•	Follows the MVC pattern architecture
•	Offers support for static template and Angular template
•	Support for two-way data-binding
•	Supports dependency injection, RESTful services, and validations


Disadvantages of Using Angular?
 Not as a disadvantage, but in some scenarios, Angular may not be the right fit. For example, for short-term projects or light-weight websites that have more static content do not require a complex framework like Angular.


What is 1TypeScript?
•	TypeScript is a typed superset of JavaScript created by Microsoft.
•	That adds optional types, classes, async/await, and many other features
•	Angular built entirely in TypeScript and used as a primary language.

npm install -g typescript

•	TypeScript provides a complete feature of an object-oriented programming language such as classes, interfaces, inheritance, modules, etc. 
•	In TypeScript, we can write code for both client-side as well as server-side development.

Why Should We Use TypeScript?
•	TypeScript simplifies JavaScript code, making it easier to read and debug.
•	TypeScript is open source.
•	TypeScript makes code easier to read and understand.
•	With TypeScript, we can make a huge improvement over plain JavaScript.
•	TypeScript gives us all the benefits of ES6 (ECMAScript 6), plus more productivity.
•	TypeScript can help us to avoid painful bugs that developers commonly run into when writing JavaScript by type checking the code.
•	Powerful type system, including generics.
•	TypeScript is nothing but JavaScript with some additional features.
•	Structural, rather than nominal.
•	TypeScript code can be compiled as per ES5 and ES6 standards to support the latest browser.
•	Starts and ends with JavaScript.
•	Supports static typing.
•	TypeScript will save developer’s time.
•	TypeScript is a superset of ES3, ES5, and ES6.
Additional Features of TypeScript
•	Functions with optional parameters.
•	Functions with REST parameters.
•	Generics support.
•	Modules support.

1Static Typing
 	The lack of static typing is JavaScript’s strength and its weakness. 
 	It makes the language very flexible, but also very error-prone. 
 	TypeScript introduces the concept of static typing to JavaScript. 
 	It’s as simple as this, when you don’t assign a variable’s data type by typing var variablename, TypeScript tries its best to infer its data type using whatever the variable is assigned to. 
 	If it’s unable to determine the data type, it assigns it the any data type.
 	You can go one step further, and assign specific data types to your variables. 
 	data types can be Boolean, Number, String, Array, Enum, Void, or Any. 
 	You can also assign an object type as a data type.


1EcmaScript features: 1ES
Some of the highlights:
1.	Arrow Functions
2.	Template Strings -ES6 introduces a new type of string literal that is marked with back ticks (`)
console.log(`hello my name is ${name}, and I am ${age} years old`);
3.	Let and const variable introduced
4.	Spread operators and Rest operators
5.	Default parameter values  Eg. Fun iodd(a, b=2)
6.	The For/Of Loop – Eg. for (variable of iterable) {
7.	isNaN() Method
8.	Array.flat()
9.	Array.find()
10.	Array.findIndex()
11.	Chaining Operator (?.)
The Optional Chaining Operator returns undefined if an object is undefined or null (instead of throwing an error).
12.	Nullish Coalescing Operator (??) – 
The ?? operator returns the first argument if it is not nullish (null or undefined). Otherwise it returns the second.
13.	Destructuring Assignment – 
//Array Destructuring
let fruits = ["Apple", "Banana"];
let [a, b] = fruits; // Array destructuring assignment
console.log(a, b);

//Object Destructuring
let person = {name: "Peter", age: 28};
let {name, age} = person; // Object destructuring assignment
console.log(name, age);

1Code Splitting
•	Code splitting allows you to split your code into various bundles which can then be loaded on demand. If used correctly, can have a major impact on load time.
Code splitting can be done at two levels: 
1.	The component level
2.	The route level. 
In component-level code splitting, you move components to their own JavaScript chunks and load them lazily when they are needed. 
In route-level code splitting, you encapsulate the functionality of each route into a separate chunk

TypeScript 1Inheritance
•	Inheritance is a fundamental concept in object-oriented programming (OOP). 
•	It allows one class to inherit properties and methods from another class. 
•	The class that inherits is called the child class, and the class whose properties and methods are inherited is called the parent class. 
•	Inheritance enables code reusability, allowing a class to leverage the functionality of an existing class without rewriting it.

class Vehicle{
    honk(): void{
        console.log("Vehicle Honks");
    }
}
class Car extends Vehicle{
    display(): void{
        console.log("This is a Car");
    }
}
let car = new Car();
car.honk();
car.display();

Output: 
Vehicle Honks
This is a Car
Explanation: Here, class Car inherits the honk() method from the Vehicle class. This way the Car class can reuse the methods of its parent class.
What are Angular 1expressions?
•	Angular expressions are code snippets that are usually placed in binding such as {{ expression }} similar to JavaScript. 
•	These expressions are used to bind application data to HTML
What are angular 1elements?
Angular elements are Angular components packaged as custom elements(a web standard for defining new HTML elements in a framework-agnostic way). Angular Elements hosts an Angular component, providing a bridge between the data and logic defined in the component and standard DOM APIs, thus, providing a way to use Angular components in non-Angular environments.

What is 1ElementRef in Angular?
•	Angular ElementRef is a class and wrapper around a native DOM element object. 
•	It contains the property nativeElement, which holds the reference to the underlying DOM object. 
•	We can use it to manipulate the DOM. We use the ViewChild to get the ElementRef of an HTML element in the component class.
@ViewChild('hello', { static: false }) divHello: ElementRef;
How do you select an element in component template?
You can control any DOM element via ElementRef by injecting it into your component's constructor. i.e, The component should have constructor with ElementRef parameter,
constructor(el: ElementRef) {
   el.nativeElement.style.backgroundColor = 'yellow';
}


What Is 1ViewEncapsulation in Angular?
It is a mechanism that 1encapsulates the styles defined in a component to prevent them from affecting other components in the application.
Angular provides three encapsulation strategies:
1.	ViewEncapsulation.Emulated (Default)
2.	ViewEncapsulation.ShadowDom
3.	ViewEncapsulation.None
Emulated:
•	Angular modifies the component's CSS selectors so that they are only applied to the component's view and do not affect other elements in the application
ShadowDom:
•	This mode uses the native browser’s shadow DOM implementation to encapsulate the styles. 
•	It requires the browser to support the shadow DOM. 
•	With this mode, the component’s styles are truly isolated within the component and do not leak out to other components or the global styles. 
•	ViewEncapsulation.ShadowDom will add the css style inside the generated DOM of your component.
None:
•	In this mode, styles defined in a component’s template are not encapsulated and can affect the entire application. 
•	It’s important to use this mode with caution.
import { Component, ViewEncapsulation } from ‘@angular/core’;

@Component({
// ...
encapsulation: ViewEncapsulation.None,
export class HelloComponent {
// ...
}

What are 1directives in Angular?
•	Directives are element which change the behavior of the dom element.
•	A directive is a class in Angular that is declared with a @Directive decorator.
•	Every directive has its own behaviour and can be imported into various components of an application.
Types of directives:
1.	Component Directives
2.	Structural Directives
3.	Attribute Directives

1. Component directives
These form the main class in directives. Instead of @Directive decorator we use @Component decorator to declare these directives. These directives have a view, a stylesheet and a selector property.

2. Structural directives
•	These directives are generally used to manipulate DOM elements.
•	Every structural directive has a ‘*’ sign before them.
•	We can apply these directives to any DOM element.

Let’s see some built-in structural directives in action:
    
      <div *ngIf="isReady" class="display_name">
          {{name}}
      </div>


      <div class="details" *ngFor="let x of details" >
          <p>{{x.name}}</p>
          <p> {{x.address}}</p>
          <p>{{x.age}}</p>
      </div>
    
  
In the above example, we can *ngIf and *ngFor directives being used.

*ngIf is used to check a boolean value and if it’s truthy, the div element will be displayed.

*ngFor is used to iterate over a list and display each item of the list.

It’s not possible to apply two structural directives to the same element.
We have moved the ngIf directive to an outer wrapping div, but in order for this to work we have to create that extra div element.

3. Attribute Directives
•	These directives are used to change the look and behaviour of a DOM element.
•	Some of the commonly used attribute directives in Angular are:
ngClass, ngStyle, ngSwitch, ngModel.


<ul *ngFor="let item of items">
  <li class="item" [ngStyle]="{'backgroundColor':getBgColor(item.type)}" > 
    {{item.name}}
  </li>
</ul>


export class ItemsComponent {
  public items = [
    {id:1,name:'APPLE',type:'fruit'},
    {id:1,name:'TURNIP',type:'vegetable'},
    {id:1,name:'ORANGE',type:'fruit'}
  ];
  public getBgColor(type){
    if(type == 'fruit'){
      return 'blue';
    }else{
      return 'green';
    }
  }
}

<h4>NgClass</h4>
<ul *ngFor="let person of people">
  <li [ngClass]="{
    'text-success':person.country === 'UK',
    'text-primary':person.country === 'USA',
    'text-danger':person.country === 'HK'
  }">{{ person.name }} ({{ person.country }})
  </li>
</ul>

Is there a way to apply a structural directive to a section of the page without having to create an extra element?
Yes and that is exactly what the ng-container structural directive allows us to do!

<ng-container *ngIf="lessons">
    <div class="lesson" *ngFor="let lesson of lessons">
        <div class="lesson-detail">
            {{lesson | json}}
        </div>
    </div>
</ng-container>

What is the purpose of ngFor directive?
We use Angular ngFor directive in the template to display each item in the list. 
For example, here we iterate over list of users,
<li *ngFor="let user of users">
  {{ user }}
</li>

What is the purpose of ngIf directive?
The Angular ngIf directive inserts or removes an element based on a truthy/falsy condition. 
Let's take an example to display a message if the user age is more than 18,
<p *ngIf="user.age > 18">You are not eligible for student pass!</p>

Note: Angular isn't showing and hiding the message. It is adding and removing the paragraph element from the DOM. That improves performance, especially in the larger projects with many data bindings.

When to use a directive?
Consider an application, where multiple components need to have similar functionalities. In this situation, one can create a directive having the required functionality and then, import the directive to components which require this functionality.

How to create a 1custom directive?
•	Creating a custom directive is just like creating an Angular component. 
•	To create a custom directive we have to replace @Component decorator with @Directive decorator.

In the command terminal, navigate to the directory of the angular app and type the following command to generate a directive:

ng g directive autoFocus
The following directive will be generated. Manipulate the directive to look like this:
    
      import { Directive, ElementRef } from '@angular/core';

      @Directive({
       selector: '[autoFocus]'
      })
      export class AutoFocusDirective implements AfterViewInit {
       constructor(el:ElementRef) { }
	 
	ngAfterViewInit() {
		if (this.el.nativeElement.outerHTML.indexOf('autofocus') > 0) {
      this.el.nativeElement.focus();
    }
}
      }
    
  
Now we can apply the above directive to any DOM element:
    
      <p [autoFocus]=autoFocus >Hello World!</p>    
Here, we are importing Directive and ElementRef from Angular core. The Directive provides the functionality of @Directive decorator in which we provide its property selector to  autoFocus  so that we can use this selector anywhere in the application. We are also importing the ElementRef which is responsible for accessing the DOM element.

What are the differences between Component and Directive?

What is 1data binding?
•	Data binding is a core concept in Angular and allows to define communication between a component and the DOM
There are 4 forms of data binding(divided as 3 categories) which differ in the way the data is flowing.
1.	String Interpolation binding
2.	Property Data Binding
3.	Event Data Binding
4.	Two-way Data binding
I. From the Component to the DOM:
1.	String Interpolation: {{ value }}: Adds the value of a property from the component
<li>Name: {{ user.name }}</li>
<li>Address: {{ user.address }}</li>
2.	Property binding: [property]=”value”: The value is passed from the component to the specified property or simple HTML attribute
<input type="email" [value]="user.email">

II. From the DOM to the Component: 
3.	Event binding: (event)=”function”: When a specific DOM event happens (eg.: click, change, keyup), call the specified method in the component
<button (click)="logout()"></button>
III. Two-way binding: 
4.	Two-way data binding: [(ngModel)]=”value”: Two-way data binding allows to have the data flow both ways. For example, in the below code snippet, both the email DOM input and component email property are in sync
<input type="email" [(ngModel)]="user.email">

What are the key 1components of Angular?
Angular has the below key components,
•	Component: These are the basic building blocks of angular application to control HTML views.
•	Modules: Modules are logical boundaries in your application and the application is divided into separate modules to separate the functionality of your application
•	Templates: This represent the views of an Angular application.
•	Services: A service is used when a common functionality needs to be provided to various modules. 
•	Metadata: This can be used to add more data to an Angular class.




Explain Components, Modules and Services in Angular

1Components:

Components are utilized to build the UI of the application; thus, components control the look and feel of the Angular Application. 

A component is defined using the @Component decorator. 

Every component consists of three parts-

•	Template − This is used to render the view for the application. This contains the HTML that needs to be rendered in the application. This part also includes the binding and directives.
•	Class − This is like a class defined in any language such as C. This contains properties and methods. This has the code which is used to support the view. It is defined in TypeScript.
•	Metadata − This has the extra data defined for the Angular class. It is defined with a decorator.
This is used to decorate Angular class with additional information.

For creating a component, inside the command terminal, navigate to the directory of the application created, and run the following command:

ng generate component test
Or
ng g c test

One can see the generated component inside src/app/test folder. The component will be defined inside test.component.ts and this is how it looks:
    
      
import { Component, OnInit } from '@angular/core';

      @Component({
        selector: 'app-test',
        templateUrl: './test.component.html',
        styleUrls: ['./test.component.css']
      })
      export lass TestComponent implements OnInit {

        constructor() {}

        ngOnInit() {
        }
      }
    
  
As we can see in the above image, our component is defined with @Component decorator.

1Modules:
Modules are logical boundaries in your application and the application is divided into separate modules to separate the functionality of your application. 
Every module is defined with a @NgModule decorator.
By default, modules are of two types:
1.	Root Module
2.	Feature Module 

•	Every application can have only one root module whereas, it can have one or more feature modules.

•	A root module imports BrowserModule, whereas a feature module imports CommonModule.

•	In the application that we created before, one can see that the root module is defined inside app.module.ts and this is how it looks:

    
      import { BrowserModule } from '@angular/platform-browser';
      import { NgModule } from '@angular/core';

      import { AppComponent } from './app.component';
      import { TestComponent } from './test/text.component';

      @NgModule({
        declarations: [
          AppComponent,
          TestComponent
        ],
        imports: [
          BrowserModule
        ],
        providers: [],
        bootstrap: [AppComponent]
      })
      export class AppModule { }
    
  
Four default important options:
1.	The declarations option is used to define components in the respective module
2.	The imports option is used to import other dependent modules. The BrowserModule is required by default for any web based angular application
3.	The bootstrap option tells Angular which Component to bootstrap in the application
4.	The providers option is used to configure set of injectable objects that are available in the injector of this module.
•	1providers: Services present in one of the modules which are to be used in the other modules or components. Once a service is included in the providers it becomes accessible in all parts of that application
•	1exports: The classes that should be accessible to the components of other modules.
•	bootstrap: The root component which is the main view of the application. This root module only has this property and it indicates the component that is to be bootstrapped.


To create a feature module, run the following command:
ng g m test-module
The module is created inside the src/app/test-module/test-module.module.ts file:
    
      import { NgModule } from '@angular/core';
      import { CommonModule } from '@angular/common';

      @NgModule({
        declarations: [],
        importts: [
          CommonModule
        ]
      })
      export class TestModuleModule { }
    
  
As one can see, CommonModule is imported since this is a feature module.


1Services :	
•	A service is used when a common functionality needs to be provided to various modules.
•	Services are objects which get instantiated only once during the lifetime of an application. 
•	The main objective of a service is to share data, functions with different components of an Angular application.
•	A service is defined using a @Injectable decorator. A function defined inside a service can be invoked from any component or directive.

To create a service, run the following command:

ng g s test-service

The service will be created inside src/app/test-service.service.ts:
    
      import { Injectable } from '@angular/core';

      @Injectable({
        providedIn: 'root'
      })
      export class TestServiceService {

        constructor() { }

      }
    
  
Any method/function defined inside the TestServiceService class can be directly used inside any component by just importing the service.

What are 1lifecycle 1hooks available?
Angular application goes through an entire set of processes or has a lifecycle right from its initiation to the end of the application.

constructor: It is invoked when a component or directive is created by calling new on the class.
1.	ngOnChanges:  It is invoked whenever there is a change or update in any of the input properties of the component.

2.	ngOnInit: It is invoked every time a given component is initialized.

3.	ngDoCheck: Called during every change detection run. This is for the detection and to act on changes that Angular can't detect on its own.

4.	ngAfterContentInit: Called after content (ng-content) has been projected into view. It response after Angular projects external content into the component's view.

5.	ngAfterContentChecked:  Called every time the projected content has been checked. It response after Angular checks the content projected into the component.

6.	ngAfterViewInit: Called after the component’s view (and child views) has been initialized. It response after Angular initializes the component's views and child views.

7.	ngAfterViewChecked: Called every time the view (and child views) have been checked. It response after Angular checks the component's views and child views.

8.	ngOnDestroy: Called once the component is about to be destroyed. Cleanup just  before the component is destroyed by Angular. You can use this hook in order to unsubscribe observables and detach event handlers for avoiding any kind of memory leaks.

What are 1decorators in angular?

•	Decorators are functions that are invoked with a prefixed @ symbol, and immediately followed by a class , parameter, method or property.
•	The decorator function is supplied information about the class , parameter or method, and the decorator function returns something in its place, or manipulates its target in some way.


What is 1metadata?
•	Metadata is used to decorate a class so that it can configure the expected behavior of the class. 
•	The metadata is represented by decorators
Class decorators, e.g. @Component and @NgModule
Property decorators Used for properties inside classes, e.g. @Input and @Output
Method decorators Used for methods inside classes, e.g. @HostListener
Parameter decorators Used for parameters inside class constructors, e.g. @Inject, Optional

What Are 1HostBinding() and 1HostListener() in Angular?

@HostBinding and @HostListener are two decorators in Angular that can be really useful in custom directives. 

The @HostBinding() function decorator allows you to set the properties of the host element in directive class.
The @HostListener() function decorator allows you to handle events of the host element in directive class.
Examples:
@HostBinding('style.border') border: string;
@HostListener('mouseover') onMouseOver() {
    this.border = '5px solid green';
}

import { Directive, ElementRef, Renderer, HostListener } from '@angular/core';
@Directive({
    selector: '[appChbgcolor]'
})
export class ChangeBgColorDirective {
    constructor(private el: ElementRef, private renderer: Renderer) {
        // this.ChangeBgColor('red');
    }
    @HostListener('mouseover') onMouseOver() {
   	this.ChangeBgColor('red');
    }
    @HostListener('click') onClick() {
        window.alert('Host Element Clicked');
    }
    @HostListener('mouseleave') onMouseLeave() {
        this.ChangeBgColor('black');
    }
    ChangeBgColor(color: string) {
        this.renderer.setElementStyle(this.el.nativeElement, 'color', color);
    }
}


What is angular CLI?
Angular CLI(Command Line Interface) is a command line interface to build angular apps using nodejs style (commonJs) modules. 
You need to install using below npm command,
npm install @angular/cli@latest



What is the difference between 1constructor and ngOnInit?
•	Constructor which is normally used for the initialization purpose. 
•	TypeScript classes HostListener has a default method called constructor 
Whereas ngOnInit method is specific to Angular, especially used to define Angular bindings. 
Even though constructor getting called first, it is preferred to move all of your Angular bindings to ngOnInit method.
In order to use ngOnInit, you need to implement OnInit interface as below,
export class App implements OnInit{
  constructor(){
     //called first time before the ngOnInit()
  }
  ngOnInit(){
     //called after the constructor and called  after the first ngOnChanges()
  }
}

What are 1pipes?
A pipe takes data as input and transforms it into desired output. 
For example, let us take a pipe to transform a component's birthday property into a human-friendly date using date pipe.
import { Component } from '@angular/core';

@Component({
  selector: 'app-birthday',
  template: `<p>Birthday is {{ birthday | date }}</p>`
})
export class BirthdayComponent {
  birthday = new Date(1987, 6, 18); // June 18, 1987
}

<td>{{ data.DateofBirth | date: 'dd/MM/yyyy' }}</td>
<h2>{{ 'ramesh rajendran' | titlecase }}</h2> // ‘Ramesh Rajendra’

•	Pipes Provided by Angular
o	CurrencyPipe
o	DatePipe
o	DecimalPipe
o	JsonPipe
o	LowerCasePipe
o	UpperCasePipe
o	TitleCasePipe
o	PercentPipe
o	SlicePipe
o	AsyncPipe
What is the difference between 1pure and impure pipe?
Two type of pipes
1.	Pure pipe
2.	Impure pipe
A pure pipe is only called when Angular detects a change in the value. 
For example, any changes to a primitive input value (String, Number, Boolean, Symbol) or a changed object reference (Date, Array, Function, Object). 
An impure pipe is called for every change detection cycle no matter whether the value changes. i.e, An impure pipe is called often, as often as every keystroke or mouse-move.
When writing a custom pipe in Angular you can specify whether you define a pure or an impure pipe:
@Pipe({
  name: 'filterPipe', 
  pure: false/true        <----- here (default is `true`)
})
export class FilterPipe {}

What is the purpose of 1async pipe?
•	In your Angular template, you can use the async pipe to directly display data from an Observable or Promise without manually subscribing to it. 
•	The async pipe subscribes to the observable and updates the view whenever new data is emitted.
•	When the component gets destroyed, the async pipe unsubscribes automatically to avoid potential memory leaks. 
•	It ensures that the latest data is displayed in the view without needing manual subscription handling or change detection
Let’s say you have a component with an observable property, and you want to display its value in the template using the async pipe:

import { Component, OnInit } from '@angular/core';
import { Observable, interval } from 'rxjs';

@Component({
  selector: 'app-example',
  template: `
    <div>
      <p>Current Time: {{ currentTime$ | async | date:'medium' }}</p>
    </div>
  `,
})
export class ExampleComponent implements OnInit {
  currentTime$: Observable<Date>;

  ngOnInit() {
    // Create an observable that emits the current time every second
    this.currentTime$ = interval(1000).pipe(map(() => new Date()));
  }
}

What is a custom pipe?
Apart from built-inn pipes, you can write your own custom pipe with the below key characteristics,
i.	A pipe is a class decorated with pipe metadata @Pipe decorator, which you import from the core Angular library For example,
    @Pipe({name: 'myCustomPipe'})
ii.	The pipe class implements the PipeTransform interface's transform method that accepts an input value followed by optional parameters and returns the transformed value. The structure of pipeTransform would be as below,
iii.	interface PipeTransform {
iv.	  transform(value: any, ...args: any[]): any
}
v.	The @Pipe decorator allows you to define the pipe name that you'll use within template expressions. It must be a valid JavaScript identifier.


What is a parameterized pipe?
•	A pipe can accept any number of optional parameters to fine-tune its output. 
•	The parameterized pipe can be created by declaring the pipe name with a colon ( : ) and then the parameter value. 
•	If the pipe accepts multiple parameters, separate the values with colons. Let's take a birthday example with a particular format(dd/MM/yyyy):
import { Component } from '@angular/core';



How do you chain pipes?
•	You can chain pipes together in potentially useful combinations as per the needs.
•	Let's take a birthday property which uses date pipe(along with parameter) and uppercase pipes as below
import { Component } from '@angular/core';

How async and 1await work in Angular?
•	Async functions make it easy to work with asynchronous code, as they allow you to use the await keyword to wait for a promise to be resolved.
•	Remember, the await keyword is only valid inside async functions
•	In other word (An async function can contain an await expression that pauses the execution of the async function and waits for a promise to be resolved, and then resumes the async function's execution and evaluates as the resolved value)

Asynchronous code: 
•	We simply mean that the code isn't executed sequentially and the process involves multithreading
•	It is a form of parallel programming that executes a separate block of code without breaking the primary application thread. 
•	Running async code is useful in case of large iterations or when you have complex operations.
What are template expressions? {{ }}
•	In the property binding, a template expression appears in quotes to the right of the = symbol as in [property]="expression". 
•	In interpolation syntax, the template expression is surrounded by double curly braces {{ }}. For example, in the below interpolation, the template expression is {{username}},
<h3>{{username}}, welcome to Angular</h3>
The below javascript expressions are prohibited in template expression
i.	assignments (=, +=, -=, ...)
ii.	new
iii.	chaining expressions with ; or ,
iv.	increment and decrement operators (++ and --)
What are the list of template expression operators?
The Angular template expression language supports three special template expression operators.
i.	Pipe operator
ii.	Safe navigation operator
iii.	Non-null assertion operator
What is String 1Interpolation in Angular?
•	String Interpolation is a one-way data-binding technique that outputs the data from TypeScript code to HTML view. 
•	It is denoted using double curly braces. {{ }} 
•	This template expression helps display the data from the component to the view.



What are 1observables?
•	Observables are not part of the JavaScript language, observables are part of RxJS library. 
•	Observables are declarative which provide support for passing messages between publishers and subscribers in your application. 
•	Observables are lazy in the sense that they only execute values when someone subscribes to it.
•	They are mainly used for event handling, asynchronous programming, and handling multiple values.
For example, you define a function for publishing values, but it is not executed until a consumer subscribes to it. The subscribed consumer then receives notifications until the function completes, or until they unsubscribe.
•	The observables are created using new keyword.
Let see the simple example of observable,
import { Observable } from 'rxjs';

const observable = new Observable(observer => {
  setTimeout(() => {
    observer.next('Hello from a Observable!');
  }, 2000);
});

What is 1cold and 1hot observable?
When the data is produced by the Observable itself, we call it a cold Observable. 
When the data is produced outside the Observable, we call it a hot Observable.

What is the difference between promise and observable?

1Promise
•	A Promise handles a single event when an async operation completes or fails.

What is an 1observer?
Observer is an interface for a consumer of push-based notifications delivered by an Observable. 

A handler that implements the Observer interface for receiving observable notifications will be passed as a parameter for observable as below,
What is 1multicasting?
Multi-casting is the practice of broadcasting to a list of multiple subscribers in a single execution.

What is 1subject in Angular?
•	It maintains a list of observers and notifies all of them when a new value is emitted using the next() method.
•	It does not have an initial value, so subscribers only receive values emitted after they subscribe
•	A Subject is like an Observable, but can multicast to many Observers. 
•	Subjects are like EventEmitters: they maintain a registry of many listeners.
import { Subject } from 'rxjs';

   const subject = new Subject<number>();

   subject.subscribe({
     next: (v) => console.log(`observerA: ${v}`)
   });
   subject.subscribe({
     next: (v) => console.log(`observerB: ${v}`)
   });

   subject.next(1);
   subject.next(2);

1.	Subject - No initial value or replay available
2.	AsyncSubject - Emits latest values to subscribers on completion of the async task
3.	BehaviouralSubject - requires an initial value and emits current values to new subscribers
4.	ReplaySubject - replays a specified number of last values to new subscribers


BehaviorSubject
•	It has an initial value and will immediately emit the initial value to any subscriber as soon as they subscribe, even if no values have been emitted yet using the next() method.
•	After the initial value is emitted, it behaves like a regular Subject and notifies subscribers about new values emitted using next().
•	This is useful when you want to provide the last known value to new subscribers, such as the current state of an application or the latest data fetched from an API.

How subjects are different from observable?
•	Subject has state, it keeps a list of observers. 
•	On the other hand, an Observable is just a function that sets up observation. 
•	While Subjects are Observables, Subjects also implement an Observer interface.
•	While plain Observables are unicast (each subscribed Observer owns an independent execution of the Observable), Subjects are multicast.
In stream programming there are two main interfaces: Observable and Observer.
•	Observable is for the consumer, it can be transformed and subscribed:
observable.map(x => ...).filter(x => ...).subscribe(x => ...)

•	Observer is the interface which is used to feed an observable source:

observer.next(newItem)

•	We can create new Observable with an Observer:

var observable = Observable.create(observer => { 
    observer.next('first'); 
    observer.next('second'); 
    ... 
});
observable.map(x => ...).filter(x => ...).subscribe(x => ...)

•	we can use a Subject which implements both the Observable and the Observer interfaces:
var source = new Subject();
source.map(x => ...).filter(x => ...).subscribe(x => ...)
source.next('first')
source.next('second')

What is 1HttpClient and its benefits?
•	It is used for Performs HTTP requests. 
•	This service is available as an injectable class, with methods to perform HTTP requests
•	It will help us fetch external data, post to it, etc.
•	This is available from @angular/common/http package. 

You can import in your root module as below,
import { HttpClientModule } from '@angular/common/http';
The major advantages of HttpClient can be listed as below,
•	Contains testability features
•	Provides typed request and response objects
•	Intercept request and response
•	Supports Observable APIs
•	Supports streamlined error handling

Explain on how to use HttpClient with an example?
Below are the steps need to be followed for the usage of HttpClient.
•	Import HttpClientModule into root module:
import { HttpClientModule } from '@angular/common/http';
@NgModule({
  imports: [
    BrowserModule,
    // import HttpClientModule after BrowserModule.
    HttpClientModule,
  ],
  ......
  })
 export class AppModule {}

•	Inject the HttpClient into the application: Let's create a userProfileService(userprofile.service.ts) as an example. It also defines get method of HttpClient

import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';

const userProfileUrl: string = 'assets/data/profile.json';

@Injectable()
export class UserProfileService {
  constructor(private http: HttpClient) { }

  getUserProfile() {
    return this.http.get(this.userProfileUrl);
  }
}

•	Create a component for subscribing service: Let's create a component called UserProfileComponent(userprofile.component.ts) which inject UserProfileService and invokes the service method,

fetchUserProfile() {
  this.userProfileService.getUserProfile()
    .subscribe((data: User) => this.user = {
        id: data['userId'],
        name: data['firstName'],
        city:  data['city']
    });
}

Since the above service method returns an Observable which needs to be subscribed in the component.

What are Http 1Interceptors?
•	HttpInterceptor are part of @angular/common/http
•	Interceptors help to execute pre-processing logic before any HTTP call is made from angular application. 
•	Which inspect and transform HTTP requests from your application to the server and vice-versa on HTTP responses. 
Interceptors can be really useful for features like…
i.	Authentication
ii.	Logging
iii.	Caching
iv.	Modifying headers
To implement an interceptor, you need to create a class that’s injectable and that implements HttpInterceptor. the Interceptor calls the intercept() method.
The intercept method takes two arguments, req and next, and returns an observable of type HttpEvent.
•	req is the request object itself and is of type HttpRequest.
•	next is the http handler, of type HttpHandler. The handler has a handle method that returns our desired HttpEvent observable.
•	When the intercept() method is called Angular passes a reference to the httpRequest object. With this request, we can inspect it and modify it as necessary. Once our logic is complete, we call next.handle and return the updated request onto the application.

You can use interceptors by declaring a service class that implements the intercept() method of the HttpInterceptor interface.
@Injectable()
export class MyInterceptor implements HttpInterceptor {
    constructor() {}
    intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
        ...
    }
}
After that you can use it in your module,
@NgModule({
    ...
    providers: [
        {
            provide: HTTP_INTERCEPTORS,
            useClass: MyInterceptor,
            multi: true
        }
    ]
    ...
})
export class AppModule {}

Is multiple interceptors supported in Angular?
Yes, Angular supports multiple interceptors at a time. You could define multiple interceptors in providers property:
The interceptors will be called in the order in which they were provided. i.e, MyFirstInterceptor will be called first in the above interceptors configuration.

How do you perform 1Error handling?
If the request fails on the server or failed to reach the server due to network issues then HttpClient will return an error object instead of a successful response.
In this case, you need to handle in the component by passing error object as a second callback to subscribe() method.
Let's see how it can be handled in the component with an example,

It is always a good idea to give the user some meaningful feedback instead of displaying the raw error object returned from HttpClient.

Using catchError Operator
The catchError operator allows you to catch errors and handle them appropriately. You can return a fallback observable or rethrow the error.
import { catchError } from 'rxjs/operators';
import { of, throwError } from 'rxjs';

this.http.get('https://api.example.com/data')
  .pipe(
    catchError(error => {
      console.error('Error occurred:', error);
      return of([]); // Return a fallback value
// return throwError(error); // Propagate the error
    })
  )
  .subscribe(data => {
    console.log(data);
  });


RxJS - Pipe
pipe() function in RxJS: You can use pipes to link operators together. Pipes let you combine multiple functions into a single function.
Observable operators are composed using a pipe method known as Pipeable Operators.

What is 1RxJS library?
•	Reactive Extensions for JavaScript (RxJS) is a reactive streams library that allows you to work with asynchronous data streams.
•	Many APIs such as HttpClient produce and consume RxJS Observables and also uses operators for processing observables.
For example, you can import observables and operators for using HttpClient as below,
import { Observable, throwError } from 'rxjs';
import { catchError, retry } from 'rxjs/operators';

Observable creation functions:
•	RxJS offers a number of functions that can be used to create new observables.
•	These functions can simplify the process of creating observables from things such as events, timers, promises, and so on.

Operators
•	RxJS is mostly useful for its operators, even though the Observable is the foundation
For example, RxJS defines operators such as map(), filter(), concat(), of(), switchMap(), mergeMap(), catchError(), take(), takeUntill(), debaounceTime(), from(), tap(), retry(), forkJoin(), combileLatest()

•	1Map is basically manipulate the data in any way that you like.
forkJoin()  - 
•	It means that forkJoin allows us to group multiple observables and execute them in parallel, then return only one observable.
•	This operator is best used when you have a group of observables and only care about the final emitted value of each. 

Tap() – 
•	After a successful API request, the tap() operator will do any function you want it to perform with the response. In the example, it will just log that string.
Switchmap(): Cancels from one observable and switches to another and it sends value from the first observable to second one.
mergeMap(): use for combining two observables into one
combineLatest(): When any observable emits a value, emit the last emitted value from each.

Error handling
•	In addition to the error() handler that you provide on subscription 
•	RxJS provides the catchError operator that lets you handle known errors in the observable recipe.
Error handling
•	In addition to the error() handler that you provide on subscription 
•	RxJS provides the catchError operator that lets you handle known errors in the observable recipe.
Lodash:
A modern JavaScript utility library delivering modularity, performance & extras
•	cloneDeep
•	isEmpty
•	isEqual
•	isNumber
•	uniqBy
•	uniq
•	camelCase
•	union
•	get
•	intersection
•	chain
•	some
•	partition
What is 1subscribing?
•	An Observable instance begins publishing values only when someone subscribes to it. 
•	So you need to subscribe by calling the subscribe() method of the instance, passing an observer object to receive the notifications

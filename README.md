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


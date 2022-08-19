1.	Demonstrate a basic understanding of Angular or What is Angular

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
  
- Angular is a typescript-based web application framework used to create & build web apps
- It allows us to create Single Page Application (SPA)
- Gmail, Youtube, PayPal apps are developed using Angular

</blockquote>
</details>

2. What is meant by SPA?

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>

- It is a single web page, website, or web application that works within a web browser and loads just a single document.
- It does not need page reloading during its usage, and most of its content remains the same while only some of it needs updating.
- **Gmail**, **Facebook**, **Trello**, **Google Maps**, etc., all are Single Page Applications that offer an outstanding user experience in the browser with no page reloading.

</blockquote>
</details>

3. Angular workflow or How does Angular work or bootstrapping your angular app?

<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>
  
- Flow: `angular.json`-> `main.ts` -> `AppModule` -> `AppModule` -> `index.html`.
- Every Angular app consists of a file named `angular.json` . This file will contain all the configurations of the app. While building the app, the builder looks at this file to find the entry point of the application.

![image](https://user-images.githubusercontent.com/103101208/185569359-55632ef6-971e-47d9-a7bf-96a1de37026e.png)
  
- Inside the build section, the main property of the options object defines the entry point of the application which in this case is `main.ts`.
- `main.ts` is the entry point of the angular application. 
- The `main.ts` file creates a browser environment for the application to run, and, along with this, it also calls a function called bootstrapModule, which bootstraps the application. These two steps are performed in the following order inside the `main.ts` file:
 ![image](https://user-images.githubusercontent.com/103101208/185569651-35a2ba9f-73fc-43c6-8548-0a24daac640b.png)
- In the above line of code, `AppModule` is getting bootstrapped.
- The `AppModule` is declared in the `app.module.ts` file. This module contains declarations of all the components.
- Below is an example of `app.module.ts` file:
![image](https://user-images.githubusercontent.com/103101208/185569778-9ff0d34a-b0e2-4701-a1db-21919ebd3ad7.png)
- As one can see in the above file, `AppComponent` is getting bootstrapped.
- This component is defined in `app.component.ts` file. This file interacts with the webpage and serves data to it.
- Below is an example of `app.component.ts` file:
  
  ![image](https://user-images.githubusercontent.com/103101208/185569886-8ca076a7-6633-4d61-beb5-0d673014b347.png)

- After this, Angular calls the `index.html` file. This file consequently calls the root component that is `app-root`. 
- This is how the `index.html` file looks:
![image](https://user-images.githubusercontent.com/103101208/185569990-6c67e5b0-d9a6-4340-b2f0-dcd9a9f738c5.png)
- The HTML template of the root component is displayed inside the `<app-root>` tags.
- This is how every angular application works. Or This is how angular application get bootstrapped

  </blockquote>
</details>

4. What is a component in angular?
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Components are the basic building blocks in the Angular application. Components contain the data & UI logic that defines the view and behavior of the web application.
    
 ![image](https://user-images.githubusercontent.com/103101208/185570645-2ab168d8-9c3d-4447-a403-703222cf7814.png)

  </blockquote>

</details>

5.	Angular Components Lifecycle or Lifecycle Hooks or LifeCycle Methods
  
<details>
<summary> <b>Show Answer</b></summary>
  
<blockquote>
  
- Angular creates a component; renders it; creates and renders its children; checks it when it’s data-bound properties change; and destroys it before removing it from the DOM. These events are called "Lifecycle Hooks".
- Lifecycle Hooks:
  ![image](https://user-images.githubusercontent.com/103101208/185570891-363fb6d0-3bcd-454e-b2da-68362092fe64.png)
- `constructor()` - The constructor of the component class gets executed first, before the execution of any other lifecycle hook events. If we need to inject any dependencies into the component, then the constructor is the best place to do so.
- `ngOnChanges()` - Called whenever the input properties of the component change. It returns a SimpleChanges object which holds any current and previous property values.
- `ngOnInit()` - Called once to initialize the component and set the input properties. It initializes the component after Angular first displays the data-bound properties.
- `ngDoCheck()` - Called during all change-detection runs that Angular can't detect on its own. Also called immediately after the ngOnChanges() method.
- `ngAfterContentInit()` - Invoked once after Angular performs any content projection into the component’s view.
- `ngAfterContentChecked()` - Invoked after each time Angular checks for content projected into the component. It's called after `ngAfterContentInit()` and every subsequent `ngDoCheck()`
- `ngAfterViewInit()` - Invoked after Angular initializes the component's views and its child views.
- `ngAfterViewChecked()` - Invoked after each time Angular checks for the content projected into the component. It called after `ngAfterViewInit()` and every subsequent `ngAfterContentChecked()`
- `ngOnDestroy()` - Invoked before Angular destroys the directive or component.
![image](https://user-images.githubusercontent.com/103101208/185571059-270e2558-e7f9-48e9-8023-3cb594a8d780.png)

  ![image](https://user-images.githubusercontent.com/103101208/185581357-0f6f857b-7e47-4acc-98f4-b992a5b02f55.png)

![image](https://user-images.githubusercontent.com/103101208/185581380-9958f808-b37a-4cad-87c9-67ebb163a03c.png)

</blockquote>  

</details>

6.	What are some advantages of Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Effective cross platform development
- Two-way data binding in Angular will help users to exchange data from the component to view and from view to the component.  It will help users to establish communication bi-directionally. 
- The Angular command-line interface (CLI) makes the developer’s job easier because it offers a set of helpful tools for coding. 
- Angular offers powerful DI (dependency injection) instrument and services to resolve various productivity issues and speed up the development process.
- Modularity of angular application makes our code readable and testable

</blockquote> 

</details>
  
7.	What are the different types of directives in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
 - Component Directives - Component directives alter the details of how the component should be processed, instantiated, and used at runtime.
- Structural Directives Structural directives are used for adding, removing, or manipulating DOM elements.
- Attribute Directives - Attribute directives are used to change the look and behavior of the DOM elements.
    
<i>Custom Directive: Custom directive can also be created if any of the above directives does not solve our purpose for the requirement
    </i>

</blockquote> 

</details>
  
  
8. Structural Directives in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
 - Structural directives are used for adding, removing, or manipulating DOM elements
- Structural directives start with an asterisk (*) followed by a directive name. 
- There are three built-in structural directives - `ngIf`, `ngFor` and `ngSwitch`.
- The `ngFor` directive is used to repeat a part of the HTML template once per each item from an iterable list.
- `ngIf` directive allows us to add or remove DOM Elements based upon the Boolean expression. We can also have an else block associated with an ngIf directive.

```html
  
<div *ngIf="age > 55; else elseBlock1">
	    {{name}} is a senior citizen
</div>
<ng-template #elseBlock1>
	    {{name}} is not a senior citizen
</ng-template>
    
```
- `ngSwitch` directive lets you hide/show HTML elements depending on an expression. `NgSwitchCase` displays its element when its value matches the switch value. `NgSwitchDefault` displays its element when no sibling `NgSwitchCase` matches the switch value.
    
```html
<!-- user to enter any vowels(a, e, i o, u), print any word starting with vowels -->
<input type="text" [(ngModel)]="str" />
<div [ngSwitch]="str">
	    <div *ngSwitchCase="'a'">Entered a!! Word: Apple</div>
	    <div *ngSwitchCase="'e'"> Entered e!! Word: Egg</div>
	    <div *ngSwitchCase="'i'"> Entered i!! Word: Ice cream</div>
	    <div *ngSwitchCase="'o'"> Entered o!! Word: Orange</div>
	    <div *ngSwitchCase="'u'"> Entered u!! Word: Umberalla</div>
	    <div *ngSwitchDefault> You Entered Constant </div>
	</div>


    
```
    
    
</blockquote> 

</details>
  
9. Attribute Directives in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Attribute directives are used to change the look and behavior of the DOM elements.
- Attribute directives are enclosed with the [] square brackets
- There are two built-in attribute directives - `ngClass` and `ngStyle`
= The `ngClass` directive is used for adding or removing the CSS classes on an HTML element. It allows us to apply CSS classes dynamically based on expression evaluation.
    
```html
    
<h3 [ngClass]="'red'"> Need your attention</h3>
<div [ngClass]="['red','size20']"> Red Background, Text with Size 20px </div>
<div [ngClass]="{'red':false,'size20':true}">Text with Size 20px</div>

```
- The `ngStyle` directive allows us to dynamically change the style of HTML element based on the expression.
    
```html
Enter the username: <input type='text' [(ngModel)]='name'>
<div [ngStyle]="{'background-color':username === 'Admin' ? 'green' : 'red' }"></div>

```

</blockquote> 

</details>
  
10.	Decorators in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- Decorators are design patterns or functions that define how Angular features work. 
- Angular supports four types of decorators:
    - Class decorators
    - Property decorators
    - Method decorators
    - Parameter decorators

</blockquote> 

</details>
  
11.	Class Decorators in Angular?
  
<details>
<summary> <b>Show Answer</b></summary>
  
  <blockquote>
    
- A class decorator tells Angular if a particular class is a component or a module.
- There are various class decorators in Angular, and among them, `@Component` and `@NgModule` are widely used.
    

</blockquote> 

</details>
  
12.	@Component Decorator
  


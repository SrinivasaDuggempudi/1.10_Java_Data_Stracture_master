# java-datastracture-master
Author : Srinivasa Duggempudi.

### Table of Contents

| No. | Questions |
|---- | ---------
|1 | [Custom Stack Implementation?](#custom-stack-implementation)|
|2 | [What is the difference between AngularJS and Angular?](#what-is-the-difference-between-angularjs-and-angular)|
|3 | [What is TypeScript?](#what-is-typescript)|
|4 | [Write a pictorial diagram of Angular architecture?](#write-a-pictorial-diagram-of-angular-architecture)|
|5 | [What are the key components of Angular?](#what-are-the-key-components-of-angular)|
|6 | [What are directives?](#what-are-directives)|


1. ### Custom Stack Implementation?

    **Stack :** Stack is a linear data structure in which insertion and deletion are done at one end, called as top.
               The last element inserted is the first one to be deleted. Hence, it is called Last in First Out(LIFO) or First in Last Out(FILO) list,
               
   **Stack Operations**
   
      **1.push():** Insert the data in the stack.
      
      **2.pop():**  Removes and returns the last inserted element from the stack.
      
      **3.peek():** Returns the last inserted element without removing it.
    
    **Implementation**
     Take the three variable like top, array and capacity.
     
     ```
       public class Stack {
	int top ;
	int arr[];
	int capacity;
	
	public Stack(int size) {
		this.top = -1;
		this.arr = new int[size];
		this.capacity = size;
	}
     
     ```
     **push:**  here before adding the element to array increase the array index(top) and assign the value. 
     
    ```
      public void push(int x) {
		
		if(!isFull()) {
			top = top +1;
			arr[top] =x;
		}else {
			
			System.out.println("Stack is Full");
		}
	}
    ```
    
      **POP :**  Take the top index element of array to return and reduce the top index value.
      
      ```
        public int pop() {
		
		int element = arr[top];
		top = top-1;
		return element ;

	}
      ```
    **PEEK:**  Pick and return the top element of Array,
    
    ```
      public int peek() {
		if(isEmpty()) {
			System.out.println("Stack is Empty");
		}
		return arr[top];
	}
    
    ```
      
      
      
                

     
      
      



  **[⬆ Back to Top](#table-of-contents)**

2. ### What is the difference between AngularJS and Angular?
    Angular is a completely revived component-based framework in which an application is a tree of individual components.

    Here are some of the major differences in tabular format:-

    | AngularJS | Angular |
    |---- | ---------
    | It is based on MVC architecture| This is based on Service/Controller|
    | It uses JavaScript to build the application| Uses TypeScript to build the application|
    | Based on controllers concept| This is a component based UI approach|
    | No support for mobile platforms| Fully supports mobile platforms|
    | Difficult to build SEO friendly application| Ease to build SEO friendly applications|

  **[⬆ Back to Top](#table-of-contents)**

3. ### What is TypeScript?
    TypeScript is a strongly typed superset of JavaScript created by Microsoft that adds optional types, classes, async/await and many other features, and compiles to plain JavaScript. Angular is written entirely in TypeScript as a primary language.
    You can install TypeScript globally as
    ```cmd
    npm install -g typescript
    ```
    Let's see a simple example of TypeScript usage:-
    ```typescript
    function greeter(person: string) {
        return "Hello, " + person;
    }

    let user = "Sudheer";

    document.body.innerHTML = greeter(user);
    ```
    The greeter method allows only string type as argument.

  **[⬆ Back to Top](#table-of-contents)**

4. ### Write a pictorial diagram of Angular architecture?
    The main building blocks of an Angular application are shown in the diagram below:-
    ![ScreenShot](images/architecture.png)

  **[⬆ Back to Top](#table-of-contents)**

5. ### What are the key components of Angular?
    Angular has the key components below,
    1. **Component:** These are the basic building blocks of an Angular application to control HTML views.
    2. **Modules:** An Angular module is a set of angular basic building blocks like components, directives, services etc. An application is divided into logical pieces and each piece of code is called as "module" which perform a single task.
    3. **Templates:** These represent the views of an Angular application.
    4. **Services:** Are used to create components which can be shared across the entire application.
    5. **Metadata:** This can be used to add more data to an Angular class.

  **[⬆ Back to Top](#table-of-contents)**

6. ### What are directives?
    Directives add behaviour to an existing DOM element or an existing component instance.
    ```typescript
    import { Directive, ElementRef, Input } from '@angular/core';

    @Directive({ selector: '[myHighlight]' })
    export class HighlightDirective {
        constructor(el: ElementRef) {
           el.nativeElement.style.backgroundColor = 'yellow';
        }
    }
    ```

    Now this directive extends HTML element behavior with a yellow background as below
    ```html
    <p myHighlight>Highlight me!</p>
    ```
  **[⬆ Back to Top](#table-of-contents)**

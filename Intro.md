# Object Oriented Programming (OOP)

OOP is a way of structuring your code into objects and classes. It is a programming paradigm centered around objects rather than functions, that allows you to create modular, reusable, and scalable code. It is just a style a programming, not a new programming language or tool.

## Pillars of OOP

There are 4 main pillars of Object Oriented Programming.

1. Abstraction
2. Encapsulation
3. Inheritance
4. Polymorphism

> Before OOP we used to do procedural programming that consists of functions and operations on the data. As the program grows, it becomes harder to manage and maintain these functions and changing something in one function will affect other functions.

With OOP, we can create **objects** and **classes** that have **properties and methods**.

- **Properties** are the variables that belong to an object.
- **Methods** are the functions that operate on these variables.

---

### **_Now let's take a comprehensive overview of the basic concepts of Object Oriented Programming_**

## 1. Encapsulation

1. Let's say CAR is an object with _properties like model, color, engine specs_ etc. and methods are _start(), stop(), reverse()_ etc.

2. Think of the local storage object in your browser that allows you to store data locally. This local storage object is an object that has **properties** such as _length, variables etc_. and **methods** such as _setItem(), getItem(), removeItem() etc._

So in OOP we group variables and functions that operate on them into objects and this is what we call ENCAPSULATION. **(See example code 1)**

#### Example Code 1

---

```JavaScript
// (Procedural Programming)
let baseSalray = 30000;
let ovetime = 10;
let rate = 20;
function getWage(baseSalray, ovetime, rate) {
    return baseSalray + (ovetime * rate);
}

// (OOP)
let employee = {
    baseSalray: 30000,
    ovetime: 10,
    rate: 20,
    getWage: function () {
        return this.baseSalray + (this.ovetime * this.rate);
    }
    // you see that here we have no parameters for the getWage function as it already knows that these are the properties of this object and easily accesses them.
    /*
    UNCLE BOB SAYS:
    "The best functions are those with no parameters!"

    The fewer the number of parameters, the easier it is to use and maintain that function. So that's what encasulation do.
    */
}
employee.getWage()
```

## 2. Abstraction

Think of a DVD player as an object. It has a lot of complex logic board inside and a few buttons outside to control it. You simply interact with these buttons and don't care what happens inside the DVD player. All that complexity is hidden from you. This is abstraction in practice.

We can use the same technique to hide some of the properties and objects inside the object to reduce the complexity of our code from us.

We get couple of benifits from it:

1. It makes the interface of that object simpler.
2. It makes the code easier to maintain.
3. It reduces the impact to change code.

## 3. Inheritance

Inheritance is a mechanism that allows you to eliminate the redundant code.

For example, think of `HTML` `textbox, select element and checkbox` etc. All of these elements have a few things in common, like they all have a `name` property and they all have a `value` property, `innerHTML`, `Click event, focus event`` etc.

We can defien all these properties in one JS object and call it `HTMLElement` and other objects will inherit these properties.

## 4. Polymorphism

"Poly" means many, "morph" means from. Polymorphism is the ability of an object to take as many forms. It helps to get rid of long `if-else or switch statements`.

**For Example,** from our previous example of HTML elements, all these elements should have ability to be rendered on the webpage but the way they are rendered is different. If we want to render multiple HTML elements in a procedural programming our code would probably look like the example given below. **(See example code 2).**  
 As you see we need to write a lot of code so it looks rough. We can use Polymorphism to get rid of this nasty procedure. In OOP we can do this using polymorphism very easily.

#### Example Code 2

---

```javascript
// (procedural programming)
switch (HTMLElement) {

  case "select":{
      renderSelect();
  }

  case "input":{
      renderTextBox();
  }

  case "button":{
      renderButton();
  }

  case "checkbox":{
      renderCheckbox();
  }

  case '...' :{
    ...
  }

}

// (OOP)
Element.render(HTMLElement);
```

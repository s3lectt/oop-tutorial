# OOP-Tutorial
**Util Lib of OOP**

# Object Definition.

* Material or abstract thing that can be perceived by the senses and described through its characteristics, behaviors and current **states**.

# What is Object?

## Example using a pen:

### Attributes:
* color, 
* load, 
* capped, 
* weight

### Methods:
draw, cover, uncover

### State:
- *State* refers to the current condition of the object, such as whether the pen is capped or uncapped. The state of an object can change over time as we interact with its methods.

#### **EVERY OBJECT HAS ATTRIBUTE, METHODS AND STATE.**

# Instantiate = Generate **object** from a **class**;

## Class:
* "Classification" or blueprint of an object;
* Defines common **attributes** and methods that will be shared by an **object**.

## Object:
* It is an **instance** of a **class**.

## The **`new`** Operator:

In JavaScript, the `new` operator is used to create an instance of an object from a class. When you use `new`, it does three main things:
1. **Creates a New Object:** A new, empty object is created.
2. **Links the Object to a Prototype:** The new object’s prototype is linked to the constructor’s `prototype`.
3. **Executes the Constructor Function:** The constructor function is called with `this` bound to the new object, initializing its properties.
4. **Returns the Object:** Finally, the newly created object is returned.

### Example:

```js
// Defining the Pen class
class Pen {
    constructor() {

        this.opened = false; // Pen state
        this.weight = 50;    // Pen weight (in grams)
        this.charge = 100;   // Pen charge amount
        this.color = 'Blue'; // Pen color

    }

    // Method to open the pen
    openPen() {
        if (!this.opened) {

            this.opened = true;

            console.log('Pen Opened Successfully!');

            return true;
        }

        console.log('Unable to open an already opened pen');

        return false;
    }

    // Method to close the pen
    closePen() {
        if (this.opened) {

            this.opened = false;

            console.log('Pen Closed Successfully!');
            
            return true;
        }

        console.log('Unable to close an already closed pen');

        return false;
    }

    // Method to draw with the pen
    drawPen() {
        if (this.opened) {
            if (this.charge !== 0) {

                console.log('You drew with your pen!');

                return true;
            }

            console.log('Unable to draw with an empty pen');

            return false;
        }

        console.log('Unable to draw with a closed pen');

        return false;
    }
}

// Instantiation of the Pen class
const instance = new Pen();

// Attempt to uncap the pen
instance.openPen();

// Attempt to draw with the pen
instance.drawPen();

// Attempt to cap the pen
instance.closePen();
```

# Practical Exercises:

1. ## Change the pen's color:
- Add a `changeColor(newColor)` method that allows you to change the pen's color.
2. ## Refill the pen::
- Add a `refill(amount)` method that increases the pen's charge.
3. ## Implement a new class:
- Create a new **`Notebook`** class with attributes like `numberOfPages` and methods like `writeOnPage ()`.


# Advanced Concepts:

- **Inheritance**: Classes can inherit attributes and methods from other classes, allowing for code reuse and organization.
- **Polymorphism**: Objects can be treated as instances of their base classes, allowing flexibility and generalization in the code.
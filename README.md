# How Do I....

<br>

---
## Strings
---

<br>

**Reverse all the characters in a string (str)**
<br>
```const reversed = str.split("").reverse().join("");```

<br>

**Reverse all the words in a sentence (sent)**
<br>
```const reversed = sent.split(" ").reverse().join(" ");```

<br>

**Capitalize the first letter of a word (str)**
<br>
```const capped = str[0].toUpperCase() + str.substring(1);```

<br>

**Capitalize the first letter of every word in a sentence (sent);**
<br>
```
const arr = sent.split(" ");
const newArr = arr.map( word => str[0].toUpperCase() + str.substring(1) )
return newArr.join(" ")
```

<br>

---
## Numbers
---

<br>

**Get a random number between min and max**
<br>
```const random = Math.floor(Math.random() * (max - min + 1) + min);```

<br>

---
## Arrays
---

<br>

<br>

---
## Objects
---

<br>

**Get all the keys in an object**
<br>
ex:  ```const obj = { name: "Bob", age: 25, location: "Home" }```

```
const keys = Object.keys(obj)
// returns [ "name", "age", "location" ]
```

<br>

**Get a value from an object when the key is dynamic**
ex:  ```const obj = { name: "Bob", age: 25, location: "Home" }```

```
const key = "name"
return obj[name];    // returns "Bob"
```

<br>

<br>

---
## HTML 
---

<br>

**Select a field based on one if its attributes**
<br>
Ex: we want to select  ```<img src="logo.jpg" />```
```const elem = document.querySelector([src='logo.jpg']);```

<br>

**Set attributes for multiple HTML elements at the same time**

*Step 1: Select all the elements first:*
<br>
  ```const elems = document.querySelectorAll("p");```

*Step 2: Make an array of objects for all the attributes you want to set:*
```
    const attrs = [
      { attribute: "style",  value: "font-size: 12px; color: blue; "},
      { attribute: "class", value: "intro" }
    ]
```

<br>

*Step 3: Call this function:*
```
    function modifyElements(elems, attrs){
      elems.forEach( elem => {
        attrs.forEach( attrObj => {
          elem.setAttribute(attrObj.attribute, attrObj.value)
        })
      })
    }
```

<br>


**Get the value of all selected checkboxes in a set:**

*Step 1: Select all possible checkboxes*

```const boxes = document.querySelectorAll("input[type='checkbox']");```

*Step 2: Call this function*
```
    function getSelectedCheckbox(boxes){
      let result = []
      boxes.forEach( check => {
        if( check.checked ){
          result.push(check.value)
        }
      })
      return result
    }
```
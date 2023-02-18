# Project 7

## Original Output Image

![Original Output Image](./original%20output%20image.png)

![Task 1 Image](./ass7.1-before.png)

## Task 1: Achieve the following Output using JavaScript DOM Manipulation

![Task 1 Image](./ass7.1-after.png)

## JavaScript Code:

```js
const language = document.querySelectorAll(".main__languages a");

for (let i = 0; i < language.length; i++) {
  // Do stuff
  if (language[i].textContent.includes(2.0)) {
    language[i].remove();
  }
}
```

---

---

![Task 2 Image](./ass7.2-before.png)

## Task 2: Achieve the following Output using JavaScript DOM Manipulation

![Task 2 Image](./ass7.2-after.png)

## JavaScript Code:

```js
const targetPlaceholder = document.querySelector("input.main__form-input");
const form = document.querySelector("form");
const submitButton = document.querySelector("button.main__form-btn");
targetPlaceholder.placeholder = "iNeuron";
targetPlaceholder.removeAttribute("disabled");
submitButton.removeAttribute("disabled");
form.addEventListener("submit", (e) => {
  // e.preventDefault();
  let languageSection = document.querySelector(".main__languages");
  let createAnchorTag = document.createElement("a");
  let createAttribute = document.createAttribute("href");
  createAttribute.value = "https://www.ineuron.ai";
  createAnchorTag.setAttributeNode(createAttribute);
  createAnchorTag.innerText = targetPlaceholder.value;
  languageSection.appendChild(createAnchorTag);
});
```

# Configuring-ESLint-in-a-Node.js-Project

## Objective

The objective of this assignment was to  setting up and configuring ESLint in a Node.js project to ensure code consistency and prevent bugs.

---

### Dependencies 

- eslint ^10.0.0
- @eslint/js ^10.0.1
- globals ^17.3.0

## Steps 

### 1. Initialized a New Node.js Project

I created a new project directory and initialized it using:

```bash
mkdir eslint-node-project
cd eslint-node-project
```

### 2. Initialize a Node.js Project

I initialized the project using:

```bash
npm init -y
```
This generated a package.json file.

### 3. Install and Configure ESLint

I installed and configured ESLint using:

```bash
npm init @eslint/config
```
 Also this created the configuration file eslint.config.mjs

### 4. Modify ESLint Rules

I customized the ESLint configuration by adding specific rules to enforce consistent code style.

In eslint.config.mjs, I added: 
```bash
{
  rules: {
    semi: ["error", "always"],
    quotes: ["error", "double"]
  }
}
```
### 5. Create a JavaScript File

I created a JavaScript file to test ESLint: touch victoriasalomon.js

I added intentionally incorrect code: 
const message = 'Hello ESLint'
console.log(message)

### 6. Run ESLint

I ran ESLint using: 
```bash
npx eslint victoriasalomon.js
```
ESLint correctly detected:

- Missing semicolons
- Incorrect quotation marks
- After correcting the code:
```bash  
  const message = "Hello ESLint";
console.log(message);
```
Running ESLint again showed no errors.

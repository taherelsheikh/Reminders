### Browser Compatibility 
1 - caniuse.com 
> A website that provides data on browsers

2 - Babel
> A JS library to convert ES6 to ES5. This is called Transpilation which is the process of converting one programming language to another

---
- **node package manager (npm)**. Developers use npm to access and manage Node packages. Node packages are directories that contain JavaScript code written by other developers. You can use these packages to reduce duplication of work and avoid bugs

- **npm init** — A terminal command that creates a package.json file.
- **package.json**  — A file that contains information about a JavaScript project.
- **npm install**  — A command that installs Node packages.

___ 

### Transpilation Project 
1 - Create a **package.json** using npm
 > - Set name - babel-project
 > - description - Transpile code in a Babel project 
 
```python
npm init
```
 
2 - Install the **Babel command line** and **Babel preset environment** npm packages.

> - install: creates a folder called node_modules tat copies packages to it 
> - -D: instructes npm to add the package to devDependencies in package.json


```python
npm install babel-cli -D
npm install babel-preset-env -D
```

3 - You can specify the initial JavaScript version inside of a file named **.babelrc**

```python
touch .babelrc
```

inside .babelrd

```
{
  "presets": ["env"]
}
```

4 - In package.json, add a script called "build".
> This will transpile code in **src** folder and put it in **lib** folder

```python
...
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "build": "babel src -d lib"
}
```

5 - Run this in the terminal 

```python 
npm run build
```
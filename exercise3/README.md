# Exercise 3 - Build a React web app using `create-react-app`

## Lesson 1

### Scenario

- Create an empty React app

### Objectives

- Learn how to use a library to build a production ready React App

### Exercises

1. Install `create-react-app`:

	```
	npm install -g create-react-app
	```

2. Create a new app:

	```
	create-react-app my-app
	```
	
3. Start the new app

	```
	cd my-app
	npm start
	```
	
## Lesson 2

### Scenario

- Create a new React component

### Objectives

- Learn about how to create a functional React component
- Use `props` and how to set default values for `props`.

### Exercises

1. Create a new file in the `src` folder with the file name `Welcome.js`

2. Copy and paste this into `Welcome.js`

	```javascript
	import React from 'react'

	const Welcome = (props) => {
		return <h1>Hello, {props.name}!</h1>
	}

	Welcome.defaultProps = {
		name: 'Michael'
	}

	export default Welcome;
	```

3. Edit `App.js` and remove the `<p>` tag. Replace it with the following:

	```javascript
	<Welcome name='Sarah' />
	<Welcome name='William' />
	<Welcome />
	```

4. The web page should reload automatically. Check the web browser for the updated view.

![Screenshot](./screenshot1.png)
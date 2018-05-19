# Exercise 2: JSX, props and states

## Objectives

- Learn about JSX, Props and States

## Steps

1. Move the hello world into a separate `const`

	```javascript
	const element = <h1>Hello, world!</h1>;
	```

2. And render that piece in the code:

	```javascript
	const element = <h1>Hello, world!</h1>;

	ReactDOM.render(
	  element,
	  document.getElementById('root')
	);
	```

3. Refresh the browser page. The text `Hello, world!` should still render.

4. Let's use your name:

	```javascript
	const name = 'Michael Cheng';
	const element = <h1>Hello, {name}</h1>;
	
	ReactDOM.render(
	  element,
	  document.getElementById('root')
	);
	```
	
5. Let's use a user object

	```javascript
	const user = {
	  firstName: 'Michael',
	  lastName: 'Cheng'
	};

	function formatName(user) {
	  return user.firstName + ' ' + user.lastName;
	}
	
	const element = (
	  <h1>
	    Hello, {formatName(user)}!
	  </h1>
	);
	
	ReactDOM.render(
	  element,
	  document.getElementById('root')
	);
	```
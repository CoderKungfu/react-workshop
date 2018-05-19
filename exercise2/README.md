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

6. HTML attributes in JSX

	```javascript
	const element = (
	  <h1 className="salutation">
	    Hello, {formatName(user)}!
	  </h1>
	);
	```

	> **Warning:**
	>
	> Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.
	>
	> For example, `class` becomes `className` in JSX, and `tabindex` becomes `tabIndex`.
	
7. React elements are immutable. So we need to call render everytime something changes.

	```javascript
	function tick() {
	  const element = (
	    <div>
	      <h1>Hello, world!</h1>
	      <h2>It is {new Date().toLocaleTimeString()}.</h2>
	    </div>
	  );
	  ReactDOM.render(element, document.getElementById('root'));
	}
	
	setInterval(tick, 1000);
	```
	
	But do notice that the browser only redraw the bits that has changed (open the inspector in the browser to see the change).
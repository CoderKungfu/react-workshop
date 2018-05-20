# Exercise 2: JavaScript and JSX

## Lesson 1

### Scenario

- Extract the HTML into a `const`.

### Objectives

- Learn about use of JS expressions.

### Exercises

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

## Lesson 2

### Scenario

- Extract a part of the string into a JSX expression.

### Objectives

- Learn about string interpolation in JSX.

1. Let's use your name:

	```javascript
	const name = 'Michael Cheng';
	const element = <h1>Hello, {name}</h1>;

	ReactDOM.render(
	  element,
	  document.getElementById('root')
	);
	```

2. Let's use a user object

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

## Lesson 3

### Scenario

- Add some HTML attributes

### Objectives

- Learn how to apply HTML attributes in JSX

### Exercises

1. Update the `<script>` block with the following:

	```javascript
	const element = (
	  <h1 className="salutation">
	    Hello, {formatName(user)}!
	  </h1>
	);
	```

2. Apply a style to it

	```css
	.salutation {
		font-weight: 2em;
		color: red;
	}
	```

	> **Warning:**
	>
	> Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.
	>
	> For example, `class` becomes `className` in JSX, and `tabindex` becomes `tabIndex`.

## Lesson 4

### Scenario

- Make a ticking clock.

### Objectives

- Learn about how React renders page elements.

### Exercises

1. React elements are immutable. So we need to call render everytime something changes.
2. Update the `<script>` block with the following:

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

3. But do notice that the browser only redraw the bits that has changed (open the inspector in the browser to see the change).

## Further Readings

- https://reactjs.org/docs/introducing-jsx.html
- https://reactjs.org/docs/rendering-elements.html
- https://reactjs.org/docs/components-and-props.html
### What I will learn in this section:

- Building Components.
- Rendering mark-up with JSX.
- Managing state.
- Passing input via props.
- Debugging React apps.
### I have learnt:

- Installed and included Bootstrap in the components to use the bootstrap CSS for the React pages.
- Learnt about Fragments and also found some cool shortcuts like 'Ctrl + D' to select multiple of the same keywords for editing purposes.
- I have learnt that you can use, '.map' to convert a list of items into a specific html component/ tag.
- The code below shows a logical AND operation being preformed:

```tsx
      function ListGroup() {
		let items = ["America", "United Kingdom", "India", "Canada", "France"];
		items = [];
		
		return (
			<>
				<h1>List:</h1>
				{items.length === 0 && <p>No items found.</p>}
				
				<ul className="list-group">
					{items.map((item) => (
						<li key={item} className="list-group-item">
							{item}
						</li>
					))}
				</ul>
			</>
		);
	}

	export default ListGroup;
```

If the first condition is true then the second condition will be returned else it will continue with the rest of the code and return all the items in the list as a, 'li' tag with the class name 'list-group-item'.
	
```tsx
	{items.length === 0 && <p>No items found.</p>}
```

- I have just learnt about 'useState'. It returns an array with two indexes. Index 0 is the actual read-only property and Index 1 is the updater function for the property at Index 0. You can see me calling 'useState' below:

```tsx
	const [selectedIndex, setSelectedIndex] = useState(-1);
```

Each time this component is called it will have it's own unique useState and will not conflict with other instances of the same component.

- Now I have been taught about Props and how we can pass data through them for functionalities sake. Below is an example of how to define a Prop and how it can be used:

```tsx
	// Prop Defined
	interface Props {
	  items: string[];
	  heading: string;
	}

	// Passing the prop to a component
	function ListGroup({ items, heading }: Props) {}

	// Passing the data to the Prop
	function App() {
	  let items = ["America", "United Kingdom", "India", "Canada", "France"];
	  
		  return (
		    <div>
			    <ListGroup items={items} heading="Cities" />
			</div>
		);
	}
```

- I have now used the Prop to pass data from the child component to the parent. This way we can add unique functionality to each component.
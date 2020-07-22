# Next.js

## Window undefined

https://nextjs.org/docs/advanced-features/dynamic-import#with-no-ssr

```jsx
import dynamic from "next/dynamic";

const DynamicComponentWithNoSSR = dynamic(
	() => import("../components/hello3"),
	{ ssr: false } //Important Part
);

function Home() {
	return (
		<div>
			<Header />
			<DynamicComponentWithNoSSR />
			<p>HOME PAGE is here!</p>
		</div>
	);
}

export default Home;
```

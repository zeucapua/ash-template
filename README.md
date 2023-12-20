# ASH Stack: Project Template
Clone to start creating projects with the ASH stack.

### Built with the ASH Stack
- Astro: Full stack web framework
- Svelte: UI framework
- HTMX: AJAX library

## Manual Install
Want to make this project template from scratch? Do the following (in your terminal):

1. Initialize a new Astro project
```bash
pnpm create astro@latest my-app
```

2. Add the Svelte integration
```bash
pnpx astro add svelte
```

3. Wherever your `<head>` is (initially at `index.astro`), add the ![HTMX CDN script](https://htmx.org/docs/#installing)
```html
<html lang="en">
	<head>
        <!-- other stuff... -->
        <script src="https://unpkg.com/htmx.org@1.9.9" integrity="sha384-QFjmbokDn2DjBjq+fM+8LUIVrAgqcNW2s0PjAxHETgRn9l4fvX31ZxDxvwQnyMOX" crossorigin="anonymous"></script>
    </head>
</html
```

4. (Optional but is in the template) Install TailwindCSS for styling
```bash
pnpx astro add tailwind
```

## Basic ASH Component
If you want a deeper explanation on how this works, read this blog! (TBD) 

Let's create a countdown timer component. The user will be able to change how many
seconds it shall start with. At the end it will display a message.

***to be continued***

1. Create a new page partial for our `timer` as a `.astro` file
```js
---
// src/pages/timer.astro
import Stopwatch from "../../components/Stopwatch.svelte"; // will be made in next step

export const partial = true;
---
```

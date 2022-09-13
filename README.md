[![Netlify Status](https://api.netlify.com/api/v1/badges/1a37075c-2a9d-429f-8c63-f7cce986e52f/deploy-status)](https://app.netlify.com/sites/imba-vite/deploys)

_Bootstrapped with [imba-vite-template](https://github.com/imba/imba-vite-template)._

## What steps did I follow to deploy this to Netlify?

### 1) Click "Add new site"

<img width="273" alt="image" src="https://user-images.githubusercontent.com/1154150/189817594-fb45f6b0-ef0b-4115-bddb-67a532538987.png">

_Or go directly to https://app.netlify.com/start_

### 2) Pick "Github" (or the git provider you use)

<img width="694" alt="image" src="https://user-images.githubusercontent.com/1154150/189817746-3dd72cc3-d283-4816-84ee-79a711bb2a3c.png">

_Or, once your git provider is authorized, you can go directly to https://app.netlify.com/start/repos_

### 3) Pick the repository

Search for this repo that you want to deploy:

<img width="731" alt="image" src="https://user-images.githubusercontent.com/1154150/189818063-7f38aeef-8a44-4453-92a0-a7cd6a2ac7a3.png">

### 4) Click "Deploy site"!

The default settings are perfect. We want to run `npm run build` ✔️ and we want to publish the `dist/` directory ✔️.

<img width="699" alt="image" src="https://user-images.githubusercontent.com/1154150/189818440-e45216eb-3502-417d-9f00-0424f0ec689b.png">

### 5) Update your Netlify badge

To make the Netlify badge in this README.md file represent your site, click into the **Site settings** -> **General** -> **Status badges** and click the copy button.

Then replace the first line of the README.md file with your own status badge

<img width="1201" alt="image" src="https://user-images.githubusercontent.com/1154150/189818916-b41e823e-0bd1-4866-b1e9-f41267f96812.png">


## Code structure

### `main.imba`

In `src/main.imba` you see how [Imba styles](https://imba.io/docs/css) work. CSS is clearly scoped in Imba, so you can see [global CSS](https://imba.io/docs/css/syntax#selectors-global-selectors), tag level, and element level.

Both [assets](https://imba.io/docs/assets) and [components](https://imba.io/docs/components/) are imported and used. Finally, the web application is started by [mounting the tag](https://imba.io/docs/tags/mounting).

### `counter.imba`

In `src/components/counter.imba` you see more about how [tags](https://imba.io/docs/tags), [props](https://imba.io/docs/tags#setting-properties), [state management](https://imba.io/docs/state-management) (which is usually a big, complex topic - but is very lightweight in Imba), and inheriting from the web itself (in this case, the HTML button). There's also a [Vitest in-source component test](https://vitest.dev/guide/in-source.html), showing you how this tag is meant to be used.

### `app.css`

You don't need to use CSS files, because of the powerful scoping of [Imba styles](https://imba.io/docs/css), but this file shows how you can get the best of both worlds. It is imported and used in `src/main.imba`.

### `utils.imba`

To showcase logic without any front end interactions, there's a simple example `src/utils.imba` has in-source testing and 

### `tests/`

In `test/basic.test.imba` you see how terse and succinct the testing syntax is with Imba, using [Vitest](https://vitest.dev/). This test is in its own file with the `.test.imba` filename ending, but you can also use inline tests like in `src/components/counter.imba`.

## Recommended IDE

- [VS Code](https://code.visualstudio.com/).
- [Imba extension](https://marketplace.visualstudio.com/items?itemName=scrimba.vsimba) - which is automatically recommended if you open this repository in VSCode.

## Available Scripts

In the project directory, you can run:

### `npm dev`

Runs in development mode on `http://localhost:3000` with hot reloading, linting and detailed error output in the console, and source maps.

### `npm run build`

Builds the app for production to the `dist` folder. From here you can [deploy your app](https://imba.io/guides/deployment) to static hosting.

### `npm run preview`

_NOTE: Requires `npm run build` to have been run first._

Preview the production application from the `dist/` folder, just as it will be running on static hosting.

### `npm test`

Run and watch the tests.

### `npm run test:ui`

Run and watch the tests - and open the [Vitest UI](https://vitest.dev/guide/ui.html)

## Notes

- This app doesn't have a server. If you need a full stack web application with server logic you can use [imba base template](https://github.com/imba/imba-base-template) or check out [Vite's backend integration guide](https://vitejs.dev/guide/backend-integration.html)
- There is a temporary `src/main.js` file that is still necessary for Vite to work correctly. You don't have to do anything with this file. And this will probably be fixed in a future version of Vite.

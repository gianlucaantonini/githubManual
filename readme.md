## General info
This project is a reminder for some command I usually use to create a new repo on Github.

## Creating a Project Locally
First I create a local project in my home folder and git init:

```
mkdir projectName
cd projectName
touch projectFile.txt
git init
touch .gitignore
```

## (optional)Creating a Svelte project with Bootstrap & SCSS
First make sure you have node and npm installed

```
node -v
pnpm -v
pnpm create svelte@latest yourProjectName
cd yourProjectName
pnpm install bootstrap
pnpm dlx svelte-add@latest scss
pnpm install
```

## (optional)Install static adapter
```
pnpm i -D @sveltejs/adapter-static
```
modify your svelte.config.js with:
```
import adapter from '@sveltejs/adapter-static';

export default {
    kit: {
        adapter: adapter({
            // default options are shown. On some platforms
            // these options are set automatically — see below
            pages: 'public',
            assets: 'public',
            fallback: undefined,
            precompress: false,
            strict: true
        })
    }
};
```
create src/routes/+layout.js file and add this code:
```
// This can be false if you're using a fallback (i.e. SPA mode)
export const prerender = true;
```

## (optional)Install nprogress
```
pnpm install nprogress
```
Add this code to +layout.svelte:
```
  import {navigating} from '$app/stores'

  // NProgress css
  import 'nprogress/nprogress.css'

  NProgress.configure({
      // Full list: https://github.com/rstacruz/nprogress#configuration
      minimum: 0.1,
  })

  $: {
    if ($navigating) {
      NProgress.start();
    }
    if (!$navigating) {
      NProgress.done();
    }
  }
```


## Creating a Repository on github

```
gh repo create yourProjectName --public
```

or

```
gh repo create yourOrganizationName/yourProjectName --private
```

## Pushing your local project on github

```
git remote add origin https://github.com/yourUsername/yourProjectName.git
git branch -M main
git add --all
git commit -m 'initial commit'
git push -u origin main
```

## (Optional Reminder: Create a virtual env with virtualenv)
```bash

#(OPTIONAL)install virtualenv with pip
pip install virtualenv

#(OPTIONAL)create virtualenv in current project folder
virtualenv yourEnvName

#(OPTIONAL)activate virtualenv
#you have to reactivate everytime you open a new terminal window
source yourEnvName/bin/activate
```

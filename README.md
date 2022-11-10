This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server with yarn:

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

# Development tools

## npx husky add .husky/pre-commit "yarn lint"

The above says that in order for our commit to succeed, the yarn lint script must first run and succeed. "Succeed" in this context means no errors. It will allow you to have warnings (remember in the ESLint config a setting of 1 is a warning and 2 is an error in case you want to adjust settings).

## npx husky add .husky/pre-push "yarn build"

The above ensures that we are not allowed to push to the remote repository unless our code can successfully build. That seems like a pretty reasonable condition doesn't it? Feel free to test it by committing this change and trying to push.

## commitlint.config.js

standard convention for all our commit messages so far, let's ensure that everyone on the team is following them as well (including ourselves!). We can add a linter for our commit messages:

To configure it we will be using a set of standard defaults, the list is included explicitly in a commitlint.config.js file:

![Angular Logo](https://github.com/vercel/vercel/blob/master/packages/frameworks/logos/angular.svg)

# Angular Example

This directory is a brief example of an [Angular](https://angular.io/) app that can be deployed with Vercel and zero configuration.

## Deploy Your Own

Deploy your own Angular project with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/vercel/vercel/tree/master/examples/angular)

_Live Example: https://angular.now-examples.now.sh_

### How We Created This Example

To get started with Angular, you can use the [Angular CLI](https://cli.angular.io/) to initialize the project:

```shell
$ ng new
```

## Accessing the WordPress site locally

This example project only contains the Angular front end; it does not bundle a
WordPress installation. If you want to work against a WordPress instance while
developing locally you will need to run WordPress separately and then point the
Angular app to that instance's REST API.

1. Spin up WordPress on your machine using your preferred method. Common
   options include [Local WP](https://localwp.com/), the official
   [`wp-env`](https://developer.wordpress.org/block-editor/reference-guides/packages/packages-env/)
   Docker setup, or a custom Docker Compose stack. Make sure the site is
   reachable from the browser (for example at `http://localhost:8888`).
2. Update the Angular app to call your WordPress REST API endpoint. You can add
   any necessary URLs to the environment configuration (for example in
   `src/environments/environment.ts`) and use that value inside your services
   when making HTTP requests.
3. Start the Angular development server with `npm install` followed by
   `npm run start`, then open `http://localhost:4200`. The front end can now
   interact with the WordPress site you have running locally.

Because WordPress runs independently from this Angular example, remember to
keep both the WordPress server and the Angular dev server running whenever you
need to test the integration.

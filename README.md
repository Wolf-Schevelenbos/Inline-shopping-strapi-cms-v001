# Strapi CMS inline-shopping

As a CMS, Strapi provides a flexible and customizable platform for creating, editing, and managing content, while also providing a robust API for integrating with other applications and services.

We use Strapi version 4.25.11.

## Structure

[This diagram](https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-04/documentation/-/blob/main/Diagrams/Inline-shopping-mysql-overview-diagram.png?ref_type=heads) describes the way the data has been structured inside of this strapi project.

Include 2 roles for users with the appropriate rights:

- store owner: has rights regarding nearly everything (coordinate, item, store-item), except other users and baskets.
- authenticated: has rights relating to only (their own) shopping baskets.

## Getting started

Ensure you have:

- a mysql server running locally, named `inlineshoppingcms`
- update/create the .env file and fill in the correct database info. Get the latest `.env` file from the development team.
- all npm package of this project

```
npm i
```

Strapi comes with a full featured [Command Line Interface](https://docs.strapi.io/dev-docs/cli) (CLI) which lets you scaffold and manage your project in seconds.

### `develop`

Start your Strapi application with autoReload enabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-develop)

```
npm run strapi develop
```

### `start`

Start your Strapi application with autoReload disabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-start)

```
npm run strapi start
```

### `build`

Build your admin panel. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-build)

The `master` branch will update the GitLab repository.

The `main` branch will update the GitHub repository. With a webhook, this triggers auto-deployment. Ensure the correct web address in `config/middlewares.ts` and `config/server.ts`

```
npm run strapi build
```

### Linking with Android/Flutter

- Update/create the .env file and fill in the correct database info.
- Make sure Strapi runs on `0.0.0.0`, double check this in `server.ts`.
- Use branch [android-working-branch](https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-04/code/cms/-/tree/android-working-branch?ref_type=heads)

### Linking with web app

- Avoid CORS issues by allowing the domain.

## Deployment

Strapi gives you many possible deployment options for your project including [Strapi Cloud](https://cloud.strapi.io). Browse the [deployment section of the documentation](https://docs.strapi.io/dev-docs/deployment) to find the best solution for your use case.

```
yarn strapi deploy
```

## 📚 Learn more

- [Resource center](https://strapi.io/resource-center) - Strapi resource center.
- [Strapi documentation](https://docs.strapi.io) - Official Strapi documentation.
- [Strapi tutorials](https://strapi.io/tutorials) - List of tutorials made by the core team and the community.
- [Strapi blog](https://strapi.io/blog) - Official Strapi blog containing articles made by the Strapi team and the community.
- [Changelog](https://strapi.io/changelog) - Find out about the Strapi product updates, new features and general improvements.

Feel free to check out the [Strapi GitHub repository](https://github.com/strapi/strapi). Your feedback and contributions are welcome!

## Functionality

- Strapi headless CMS
- uses some custom controllers on "android-working-branch"
- has autodeployment on "master" branch

There are 2 working branches due to lack of time to update the different apps to be able to merge these branches. With more time this would all be on the "master" branch.

- The [master](https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-04/code/cms/-/tree/master?ref_type=heads) branch is used in the business rules microservice, firebase application and has auto-deployment.
- The [android-working-branch](https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-04/code/cms/-/tree/android-working-branch?ref_type=heads) is used to test the android app and other microservice.

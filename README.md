# :Different Assessment with React, Gatsby and Prismic

This website is created to add all the available job vacancies in :Different. Through the Prismic CMS the developer can easily upload the contnt to make it available in live to the all user. 

- **Demo**: [Open live demo][live-demo]

&nbsp;

<img src="https://user-images.githubusercontent.com/8601064/163122284-5b80a81e-a4fd-482e-9bd5-99b22f61175f.png" alt="Screenshots of the site seen on deskop and mobile browsers" />

&nbsp;

## Installation

Run the following commands in your terminal to install Prismic and Gatsby in your local machine:

```sh
npm install -g prismic-cli
npm install -g gatsby-cli
```

Start a new project, run the following command in your terminal:

```sh
npx prismic-cli@latest theme --theme-url https://github.com/vageesan23/different-assessment --conf sm.json
```

The following instructions will help to create and set up the repository and content pages in Prismic CMS:

1. Go to [Prismic.io][prismic-io].
2. Create a new profile.
3. Create a new Prismic repository with Gatsby framework. 
4. Create a new custom type in your Prismic repository.
5. Create contents provided in the custom types section in this project folder.
6. Create some content pages to the particular custom types.
7. In the Prismic previews section create a new preview as `/api/preview`.

change your project directory to your project in terminal:

```sh
cd your-project-name
```

In your gatsby-config.js file, change your repositoryName as your repository name in Prismic:

```sh
{
      resolve: "gatsby-source-prismic",
      options: {
        repositoryName: "diff-vacancy-blog",
        customTypeModels,
        sharedSliceModels,
        routes,
      },
}
```

To install the starter default theme of Prismic, run the following command:

```sh
npm install gatsby-source-prismic gatsby-plugin-prismic-previews gatsby-plugin-image gatsby-plugin-postcss
``` 

When you're ready to start your project, run the following command:

```sh
npm start
``` 

Your project will run locally in the following URL:

```sh
[http://localhost:8000][local-host]
``` 

Through this below URL you can query your data:

```sh
[http://localhost:8000/___graphql][graph-ql-host]
``` 

[prismic-io]: https://prismic.io/
[live-demo]: https://gatsby-starter-prismic-blog.vercel.app/
[local-host]: http://localhost:8000/
[graph-ql-host]: http://localhost:8000/___graphql
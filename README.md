# :Different Assessment with React, Gatsby and Prismic

This website is created to add all the job vacancies available in :Different. Through the Prismic CMS the developer can easily upload the content to make it available in live to the all users. 

- **Demo**: [Open live demo][live-demo]
&nbsp;

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/main.png?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

&nbsp;

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/careers.png?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

&nbsp;

## Installation

Run the following commands in your terminal to install Prismic and Gatsby in your local machine:

```sh
npm install -g prismic-cli
npm install -g gatsby-cli
```

To start a new project, run the following command in your terminal:

```sh
npx prismic-cli@latest theme --theme-url https://github.com/vageesan23/different-assessment --conf sm.json
```

The following instructions will help to create and set up the repository and content pages in Prismic CMS:

1. Go to [Prismic.io][prismic-io].
2. Create a new profile.
3. Create a new Prismic repository with Gatsby framework. 
&nbsp;

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/repocreate.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

4. Create a new custom type in your Prismic repository.
&nbsp;

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/customtypes.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

5. Create contents provided in the custom types section in the project folder `project-folder\customtypes`.
6. Create some content pages to the particular custom types and publish it to the live.
&nbsp;

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/contentpages.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

7. In the Prismic previews section create a new preview as `/api/preview`.
&nbsp;

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/previews.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

&nbsp;
Change your project directory to your project in terminal:

```sh
cd your-project-name
```

In your gatsby-config.js file, change your repositoryName as your repository name in Prismic:

```sh
{
      resolve: "gatsby-source-prismic",
      options: {
        repositoryName: "your-repository-name",
        customTypeModels,
        sharedSliceModels,
        routes,
      },
}
```

In your sm.json file, change your apiEndpoint as your repository endpoint in Prismic:

```sh
{
  "_latest": "0.4.2",
  "apiEndpoint": "https://your-repository-name.prismic.io/api/v2",
  "libraries": ["@/src/slices"],
  "framework": "none"
}
```

<img src="https://github.com/vageesan23/different-assessment/blob/main/images/endpointapi.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

&nbsp;
To install the starter default theme of Prismic, run the following command:

```sh
npm install gatsby-source-prismic gatsby-plugin-prismic-previews gatsby-plugin-image gatsby-plugin-postcss
``` 

To start the project, run the following command:

```sh
npm start
``` 

The project will run locally in the following URL:

```sh
http://localhost:8000/
``` 
<img src="https://github.com/vageesan23/different-assessment/blob/main/images/local.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

&nbsp;

Through this below URL you can query your data:

```sh
http://localhost:8000/___graphql/
``` 
<img src="https://github.com/vageesan23/different-assessment/blob/main/images/graphql.jpg?raw=true" alt="Screenshots of the site seen on deskop and mobile browsers" />

[prismic-io]: https://prismic.io/
[live-demo]: https://diff-vacancy-blog-oqta370jn-vageesan23.vercel.app

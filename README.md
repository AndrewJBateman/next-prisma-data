# :zap: Next Prisma Data

* Next.js React used with a Prisma database to display a simple data table
* **Note:** to open web links in a new window use: _ctrl+click on link_

![GitHub repo size](https://img.shields.io/github/repo-size/AndrewJBateman/next-prisma-data?style=plastic)
![GitHub pull requests](https://img.shields.io/github/issues-pr/AndrewJBateman/next-prisma-data?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/AndrewJBateman/next-prisma-data?style=plastic)
![GitHub last commit](https://img.shields.io/github/last-commit/AndrewJBateman/next-prisma-data?style=plastic)

## :page_facing_up: Table of contents

* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## :books: General info

* GraphQL, a query language for APIs.
* Angular [HttpInterceptor](https://angular.io/api/common/http/HttpInterceptor) used to intercept a Http request and show a spinner
* styling done using SCSS instead of Angular Material, Bootstrap, Tailwind etc.
* Dummy robots.txt file added to fool lighthouse test for Search Engine Optimization (SEO)

## :camera: Screenshots

![Frontend screenshot](./imgs/list.png)

## :signal_strength: Technologies

* [Node.js v14](https://nodejs.org/) javascript runtime using the [Chrome V8 engine](https://v8.dev/).
* [React v17](https://reactjs.org/) Javascript library.
* [Apollo v2](https://www.apollographql.com/) GraphQL implementation data graph layer
* [Next v10](https://nextjs.org/) minimalist framework for rendering react apps on the server.
* [Next with Apollo v5](https://www.npmjs.com/package/next-with-apollo) to save coding time
* [@prisma/client](https://www.npmjs.com/package/@prisma/client) auto-generated query builder that enables type-safe database access
* [Prisma Studio](https://www.prisma.io/studio)

## :floppy_disk: Setup

* Install dependencies using `npm i`
* `npm run dev` runs the Next app in the development mode. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
* `npx prisma studio` opens up a useful browser CLI for the Prisma database on `http://localhost:5555/`

## :wrench: Testing

* Run `ng test` to run Jasmine unit tests via [Karma](https://karma-runner.github.io)
* Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## :computer: Code Examples

* `pages/index.ts` async function to fetch all data from the Prisma database

```javascript
export async function getServerSideProps() {
	const movies = await prisma.movie.findMany();

	return {
		props: {
			data: movies,
		},
	};
}
```

## :cool: Features - Frontend

* The Prisma CLI browser interface is quite cool

## :clipboard: Status, Testing & To-Do List

* Status: Working
* To-Do: Change use of item.id as key in React list of films as it is not best practise

## :clap: Inspiration/General Tools

* [Tutorial de Angular 11 desde cero 📕 Curso Angular en Español - Graphql API Rick and Morty](https://www.youtube.com/watch?v=dy6GEHWLwrs)
* [Manejar Local Storage con Angular 11 - #2](https://www.youtube.com/watch?v=PgI3jo95F5c)
* [#angular Instalar NGX-TOASTR 🔔 en Angular 11 #3](https://www.youtube.com/watch?v=7UJw-PJjKuk&t=8s)
* [Scroll Infinito Angular 11 - Angular curso #4](https://www.youtube.com/watch?v=bAnUkyawtAY)
* [Efecto de carga en Angular spinner, loading - Curso práctico Angular 11 #5](https://www.youtube.com/watch?v=uQprcZ0FYMw)
* [Recuperamos details - Aplicación Ricky and morty API - Angular 11](https://www.youtube.com/watch?v=70jrlNJ3YsM)
* [¿Qué es angular universal? - Server Side Rendering (SSR) con Angular Universal](https://www.youtube.com/watch?v=2eksE5hlbmQ)
* [Primeros pasos con netlify y angular SSR](https://www.youtube.com/watch?v=Zshv21H1M2A)
* [THIRUVANANTHAPURAM: How to add eslint to angular 12 project](https://www.youtube.com/watch?v=Km7RuJEfE0c)
* [Stackoverflow: argument-of-type-null-is-not-assignable-to-parameter-angular](https://stackoverflow.com/questions/67025848/argument-of-type-null-is-not-assignable-to-parameter-angular)

## :file_folder: License

* N/A

## :envelope: Contact

* Repo created by [ABateman](https://github.com/AndrewJBateman), email: gomezbateman@yahoo.com

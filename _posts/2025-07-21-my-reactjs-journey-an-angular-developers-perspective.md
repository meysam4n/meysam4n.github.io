# My React.js Journey: An Angular Developer's Perspective

![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3wzfl9rm2dnds1m2oc36.png)

In 2017, I started working with Angular 4 as my first frontend framework, altough I was a PHP backend dev who had pretty nice experience with CSS, HTML and bootstrap.

I totally dedicated myself to build the project I was given to me from scratch while I had zero experience working with Angular and the deadline wasn't very long. However, In the end, the result was spectacular, the company was so satisfied and I learned Angular from scratch in a very short time working on a real project. I fell in love with Angular and did serveral projects with it afterward for years.

Recently, I had some very good job opportunities that required React.js and I decided to learn it, although because of Angular's beautiful structure, all of my previous efforts to get started with React had failed before. It's very hard to start a language or framework while you feel the way the framework has implemented things isn't right compared to the language or framework you know very well. However, After a couple of days struggling I finally decided to give it a chance unlike before. So, this post is about my React.js journey that I think might be useful especially for angular developers.

I divided this journey into the steps below, each step includes the concern, options and comparison with Angular.


## Framework vs Library 
React.js is a library which offers no built-in features unlike Angular, so starting React from scratch requires installing many third-party packages that make you spending more time to install necessory packages and libraries to run your app.

So I needed a React framework which saves my time having built-in features. In order to do so, I started looking for a react framework which led me to [`Next.js`](https://nextjs.org/). After a couple of days working with it, I found out it was too bloated for a single-page application (SPA), for this cause, I found [`Vite`](https://vite.dev/) very promising and I switched to it. 

Based on my experience, React doesn't have a gentler learning curve than Angular unlike what I've heard about. Maybe this applies for someone who has zero experience with other frameworks because in my case, it was the opposite.



**Side Note:**
>  React recommends using a framework that fully integrates routing into features like data-fetching and code-splitting out of the box. This avoids the pain of needing to write your own complex configurations and essentially build a framework yourself.


## Typescript
Angular comes with TypeScript by default and it's really better compared to coding in JavaScript. while you can choose TypeScript for your react project, there are many examples using JavaScript in the web which might made you confused.

## UI component library
Unlike Angular which limited to a few solid UI component libraries like `Angular Material` and `PrimeNG`, React has lots of high quality UI component libraries which took me a couple of days to check them out. because there are many options. however, I'm honestly surprised how great react components are. 

Below are the list of the most important ones in my eyes:
* [Material UI](https://mui.com/)
* [Chakra UI](https://chakra-ui.com/)
* [Radix UI](https://www.radix-ui.com/)
* [Shadcn UI](https://ui.shadcn.com/)
* [Ant Design](https://ant.design/)
* [Mantine](https://mantine.dev/)
* [DaisyUI](https://daisyui.com/)

Eventually, I settled on `Shadcn`. because of the style and their components and blocks. also having interesting templates like dashbaords had a big impact on my decision. 

**Side Note:** There are the other solid UI component libraries which I didn't mention them, because I didn't find them interesting, while they might find them interesting, so you can discover them.

## Folder structure
Then, I had to figure out the best folder structure. There were so many conflicting opinions that finally led  me to a structure like below:

```
-src
  - components 
  - context 
  - hooks
  - lang
  - lib 
  - models # or types For general TypeScript types, enums and interfaces
  - pages
    - auth
      - SignIn.tsx
  - services
    - AuthService.ts
  - utils
```

There is a feature-sliced structure folder which I didn't use it intentionally because as my first project, i didn't want to make more complicated and it wasn't necessary.

Unlike Angular which gives you a clear way of structure for your project, React has no best practice and this leads to very ugly structures that vary projects to projects!
I really love Angular's modular approach and its separation of concerns, which divides an application into distinct sections like Component, Service, and Module.

## Router
Angular comes with a built-in router that provides you a great way to route your URLs, but in React, again, you have to install a third party package like [`React Router`](https://reactrouter.com/) and [`TanStack Router`](https://tanstack.com/router/latest). After spending hours, I went with `React Router` because it's the most popular package and it's also easy to learn. Although TanStack Router seems more advanced, I didn't want to overkill my first project.

## Form and Validation
For the first time, you don't need to spend hours to read about options because there are two popular packages, [`react-hook-form`](https://react-hook-form.com/) and [`zod`](https://zod.dev/), which makes choosing so easy. The documentation is nice and you can get started so quickly.

## Multiple Languages
The most apps I've worked with, have two languages at least so the next challenge was to find a library among many to get the job done. After spending hours, [`react-i18next`](https://react.i18next.com/) attracted my attention however after reading the documentation, I realized I should write a simple library because I didn't want to spend hours to learn a package for doing a simple job and also load many packages.  

Angular's built-in package is awesome, you don't need to do anything. It includes everything you need. 


## Conclusion
To quickly summarize my journey in this article, I want to highlight the main points.
* **framework:** I started using `Vite` but you can use [`Next.js`](https://nextjs.org/), If you need server-side rendering (SSR)

* **TypeScript:** I used it by default, because it offers many features like type checking, etc.
* **UI component library:** I went with [Shadcn UI](https://ui.shadcn.com/), but there are many great options.
* **Folder structure:** If it's going to be a small-medium size project, go with a simple structure and change it as the project grows, otherwise use a feature-sliced style.
* **Router** Go with [`React Router`](https://reactrouter.com/) because it's the most popular React router right now
* **Multiple Languages:** I ended up implementing of a custom library, but you can use [`react-i18next`](https://react.i18next.com/) if you need advanced features.


 **Note:**  This journey hasn't finished. I'm going to update this article as I move forward with React


So, what are your thoughts? We're curious to hear from you in the comments section.
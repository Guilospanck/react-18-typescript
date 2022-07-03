# React v18 TypeScript
A simple template to start your new React v18 TypeScript project. It includes some of the most used features for a React TypeScript initial project.

## Features
- React v18 TypeScript
- React Router DOM
- ESLint
- Styled Components
- Recoil
- Jest
- Cypress
- Husky
- Webpack
- Babel
- GitHub Actions

## How to use
Just click in `Use this template` in order to start your new project with this code.

## Tree Hierarchy
It makes use of the concept of Clean Code Architecture in order to build a more reliable and maintainable application.

```
.
├── assets
│   └── images
├── components
│   └── Loading
├── pages
│   └── Home
│       ├── context
│       ├── types
│       ├── useCases
│       ├── viewModels
│       └── views
└── shared
```

This is just an example that I, personally, use.
We divide the files as follows:

- `assets`: as the name suggests, here lies all graphic data we may use in our application, like videos, images, svgs, gif...and so on.
- `components`: we always think in terms of componentization. By this means, every single component (like a Loading one) we use in several places in our application, we should put it in here and reuse it throughout the code.
- `pages`: usually every and each different route will have a different page. Therefore, we divide them into different folders. In this example, we have the `Home` page.
  - `context`: here we make use of React Context if the components in our page need to recall some state that lies in different components on the same page. This prevents us from cascading props.
  - `types`: every single type we use in our page, we put it all in here.
  - `useCases`: usually a useCase will have functions that communicate with our servers (like an HTTP request) or some complex objects maneuvers.
  - `viewModels`: in order for our view to not be static, it must have some definitions and actions, like updating it at some rate; onClick events; websocket events and others. Therefore, here lies all things needed to make the page (the view) dynamic.
  - `views`: only the UI must exist in this folder. It's only what the user will see, like HTML and CSS.
- `shared`: every other element that is used by more than one page, subject or component must exist here.
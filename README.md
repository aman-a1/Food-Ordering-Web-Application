# foodapp

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

1. Cause the web application runs on Vue.js, install Vue.js globally.

npm install -g @vue/cli

2. To install the dependices and node modules, just go into the foodapp folder and then type the npm command.

npm install

3. To run the app, you need to start the vue server, just go into the foodapp folder and then type the npm command then go to the localhost (127.0.0.1:8080)

npm run serve

4. Most of the Vuejs pages share a similar structure, as the template(contains all the visual elements (HTML)) is at the top and the script (JS) is at the bottom.
   No need to mess around with the CSS unless you want to, as I have created a seperate folder for CSS.
   Additionally, bootstrap components have there own css built in, so we dont have to write any.

Dependencies and API.

Meaning of each file and folder

1.Public - Has the images for the website.

2.Assets - Has the CSS (Not that important, cuz bootstrap takes care of it)

3.Components - Contains different website components
i. HelloWorld.vue - Basic Vue.js pages, you can copy paste into a new componenet for a starting off template
ii. Hero.vue - Main landing page the user sees
iii. Login.vue - Login component

https://firebase.google.com/docs/auth/web/password-auth
https://firebase.google.com/docs/reference/js/firebase.auth.Auth#signinwithemailandpassword

iv. Navbar.vue - Navbar component

4. Router - Vue-Router (VERY IMPORTANT- connects and redirects different components and views to each other)
   Just import whatever component or view you want to use and add it to the routes array.

The overview and products views are children of the admin view. This means that the user has to have access to the admin view in order to view the products and overview view.
(kinda like a subdirectory which requires auth)

https://router.vuejs.org/guide/advanced/meta.html

5. Sections - Contains elements of the main landing page.

6. Views - Contains different views the user will come across while using the website

i. About.vue - About page
ii. Admin.vue - User dashboard user has access to after logging in.
iii. Home.vue - Footer of the main landing page.
iv. Overview.vue - Part of the user dashboard
v. Products.vue - Displays user resteraunt products.

I used firestore in order to communicate with the collection('products').

Not Real time

https://firebase.google.com/docs/firestore/quickstart - adding data

https://firebase.google.com/docs/firestore/query-data/get-data - reading data

https://firebase.google.com/docs/firestore/manage-data/delete-data - deleting data

https://firebase.google.com/docs/firestore/manage-data/add-data - update data

Real Time (with Vue-firestore)

https://alligator.io/vuejs/vue-cloud-firestore/
https://github.com/gdg-tangier/vue-firestore

7. firebase.js - firebase auth elements which connect our code to the firebase server.

8. Main.js - api's and components being used across multiple files and folders. Kinda like global variables, as in all files will have access to the imports.

IMP - All importants and everything should be before the mounting part.(new Vue)

https://firebase.google.com/docs/auth/web/manage-users

Bootstrap - Bootstrap has prebuilt templated ui-visual-elements which makes it easier as we have to write less code. So far, I have used Navbar and Modal boostrap components.

Theres other bootstrap ui-components we can use - https://getbootstrap.com/docs/4.4/getting-started/introduction/

SweetAlert - Animations (The tick and x and all that - looks cool)

https://sweetalert2.github.io/

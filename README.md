# Flask React Project

NOTES 
* Feel free to delete, comment out, modify etc. to suit your needs. 
* The Table of Contents ('TOC') was auto-generated with Markdown-Preview, a VSCode Plugin.
* I included some fake examples for some portions, like UI / UX, seeder data, etc, as well as
links to potentially helpful resources, in comments. 
* Other portions, like the tables and routes, have been filled using the content of the
Flask starter template provided by instructor Bart Dorsey.

## TABLE OF CONTENTS
<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->
- [Updates](#updates)
- [About](#about)
  - [Team](#team)
  - [Description](#description)
  - [Screenshots](#screenshots)
    - [Splash Page](#splash-page)
    - [Product Page](#product-page)
  - [Code Samples](#code-samples)
    - [Snippet 1: Warping time-space with an algorithm](#snippet-1-warping-time-space-with-an-algorithm)
    - [Snippet 2: A custom reusable 'type' input component](#snippet-2-a-custom-reusable-type-input-component)
- [Technologies](#technologies)
  - [React Components](#react-components)
- [Features](#features)
  - [MVPs](#mvps)
  - [Major Stretch Goals](#major-stretch-goals)
  - [Minor Stretch Goals](#minor-stretch-goals)
  - [Ideas & Notes](#ideas-notes)
- [Models & Schema](#models-schema)
  - [Full Schema](#full-schema)
  - [Tables](#tables)
    - [`users`](#users)
    - [`table_name_here...`](#table_name_here)
- [Routes](#routes)
  - [Backend Routes](#backend-routes)
    - [`/api/auth`](#apiauth)
    - [`/api/users`](#apiusers)
    - [`/api/...`](#api)
  - [Frontend Routes](#frontend-routes)
- [UI / UX](#ui-ux)
  - [Wireframe Sketches](#wireframe-sketches)
    - [Mobile / Portrait](#mobile-portrait)
    - [Desktop / Landscape](#desktop-landscape)
  - [Styling](#styling)
    - [Colors](#colors)
    - [Fonts](#fonts)
    - [Assets](#assets)
- [Required Seeder Data](#required-seeder-data)
  - [`users`](#users-1)
  - [`products`](#products)
  - [`favorites`](#favorites)
- [Local Setup](#local-setup)
- [Getting started](#getting-started)
- [Deploy to Heroku](#deploy-to-heroku)

<!-- /code_chunk_output -->

## Updates
01/01/21 Notes here about any recent major updates, plans, or news.


## About
### Team
* Name [GitHub](github-link-here) [LinkedIn](linkedin-link-here) [Website](link-here)
* Name [GitHub](github-link-here) [LinkedIn](linkedin-link-here) [Website](link-here)

### Description
**INSPIRATIONS**
* [insert app here](https://www.pinterest.com/)
<!-- If your site is a clone, or you have any inspirations heavily referenced
for the project, you can list them here if you want. -->
A quick summary of what your app is, what makes it unique, who its intended for, et cetera.

**USER STORY**
<!-- Wikipedia: User Story - https://en.wikipedia.org/wiki/User_story -->
* As a *role* I can *capability*, so that *receive benefit*.
* *As a* garden hobbyist, *I can* browse and filter through a selection of products by plant type, *so that* I can easily find and purchase plants I'm interested in.

### Screenshots
#### Splash Page
![screenshot 1](https://cdn190.picsart.com/230601303016212.png?type=webp&to=crop&r=256)
<!-- NOTE Change links to your own local image paths -->
Add potential notes here.

#### Product Page
![screenshot 2](https://cdn190.picsart.com/230601303016212.png?type=webp&to=crop&r=256)
Add potential notes here.


### Code Samples
#### Snippet 1: Warping time-space with an algorithm
``` python
def cool_snippet_here():
    """This cool snippet opens a time-space warphole with just code!"""
    print("Abra kadabra, two great Pokemon.") # Prints a statement to the terminal
    return true # Note, does not return false
```

#### Snippet 2: A custom reusable 'type' input component 
``` js
function CustomTextInput({label, value, handleChange}) {
  return (
    <label className="custom-text-style fancy cool">{label}
      <input type="text" value={value} onChange={handleChange} />
    </label>
    <small>Character max limit: 500</small> 
  )
}
```
Small, reusable input components like this were built and applied liberally to forms throughout the site, forming a small library of form-input components. Since the styling direction changed often, building these mini-components early helped with adapting to such updates immensely.

--------------------------------------------------------------------------------
## Technologies
* Python
* JavaScript
* PostgreSQL
* Flask
* SQLAlchemy
* WTForms & Flask-WTF
* React
* Redux

### React Components
* ...

--------------------------------------------------------------------------------
## Features
### MVPs
* User accounts: signup, login, logout
* ...

### Major Stretch Goals
* ...

### Minor Stretch Goals
* ...

### Ideas & Notes
* ...


--------------------------------------------------------------------------------
## Models & Schema
### Full Schema
[See Online Diagram](https://dbdiagram.io/) 
<!-- NOTE Change the link to your own diagram -->

![schema](https://cdn190.picsart.com/230601303016212.png?type=webp&to=crop&r=256)


### Tables
* users
* ...table_name_here...

#### `users`
| COLUMN          | DATA TYPE    | CONSTRAINTS      |
|-----------------|--------------|------------------|
| id              | integer      | serial, pk       |
| username        | varchar(50)  | not null, unique |
| email           | varchar(255) | not null, unique |
| hashed_password | varchar(255) | not null         |

#### `table_name_here...`
| COLUMN | DATA TYPE | CONSTRAINTS |
|--------|-----------|-------------|
| id     | integer   | serial, pk  |


--------------------------------------------------------------------------------
## Routes
### Backend Routes
* `/api/auth`
* `/api/users`
* `/api/...`

#### `/api/auth`
| METHOD | PATH            | NOTES                                             |
|--------|-----------------|---------------------------------------------------|
| GET    | `/`             | Authenticates a user                              |
| GET    | `/unauthorized` | Returns 401 unauthorized JSON when flask-login authentication fails |
| POST   | `/login`        | Logs a user in                                    |
| POST   | `/logout`       | Logs a user out                                   |
| POST   | `/signup`       | Creates a new user and logs them in               |

#### `/api/users`
| METHOD | PATH        | NOTES                                       |
|--------|-------------|---------------------------------------------|
| GET    | `/`         | Returns dictionary of all user dictionaries |
| GET    | `/<int:id>` | Return a user dictionary                    |

#### `/api/...`
| METHOD | PATH | NOTES |
|--------|------|-------|
| GET    | `/`  | (n/a) |


### Frontend Routes
| PATH             | COMPONENT     | NOTES            |
|------------------|---------------|------------------|
| `/`              | (n/a)         | exact, protected |
| `/users`         | UsersList     | exact, protected |
| `/users/:userId` | User          | exact, protected |
| `/login`         | LoginForm     | exact            |
| `/sign-up`       | SignUpForm    | exact            |



--------------------------------------------------------------------------------
## UI / UX
<!-- NOTE These are all purely example content. Please replace with your own 
content or comment out until you're ready. -->

### Wireframe Sketches
#### Mobile / Portrait
![Splash](insert-image-link-here)
![Home](insert-image-link-here)
![Users List](insert-image-link-here)
![User Profile](insert-image-link-here)

#### Desktop / Landscape
![Splash](insert-image-link-here)
![Home](insert-image-link-here)
![Users List](insert-image-link-here)
![User Profile](insert-image-link-here)


### Styling
<!-- NOTE Consider linking to a pinterest mood board, keywords, etc.) -->
**KEYWORDS:** examples, cute, professional, sleek, cozy, hand-crafted, minimalist, Material UI, antique, futuristic, dark, feminine, elegant, modern

**INSPIRATIONAL REFERENCES**
* [Wix Template: Prickles & Co](https://www.wix.com/website-template/view/html/1995?siteId=a51d32ee-c2eb-494c-86b9-0d1c722f9f85&metaSiteId=16dcad0e-953b-4c09-ae4a-2abc30d21d17&originUrl=https%3A%2F%2Fwww.wix.com%2Fwebsite%2Ftemplates%2Fhtml%2Fall%2F3&tpClick=view_button)
* [Website: The Sill](https://www.thesill.com/collections/all-plants)

#### Colors
<!-- 
> **Helpful Resources:**
> * https://coolors.co/
> * http://colorizer.org/ 
-->
* **Color Palette:** https://coolors.co/cae7b9-f3de8a-eb9486-7e7f9a-97a7b3
* **Primary:** #CAE7B9
* **Secondary:** #F3DE8A
* **Alert:** #EB9486

#### Fonts
<!-- 
> **Helpful Resources:**
> * https://fonts.google.com/
> * https://www.dafont.com/
> * https://www.fontspring.com/free
-->
* **Headers:** https://fonts.google.com/specimen/Roboto
* **Body:** https://fonts.google.com/specimen/Roboto+Condensed
* **Special:** https://www.dafont.com/cf-plants-and-flowers.font

#### Assets
<!-- 
> **Helpful Resources:**
> * https://www.creativebloq.com/graphic-design/best-places-free-vector-art-1012985
> * https://fontawesome.com/
> * https://www.freepik.com/
> * https://pixabay.com/
> * https://www.vecteezy.com/
> * https://commons.wikimedia.org/wiki/Main_Page
NOTE Remember to check the attribution requirements when using free assets!
Some sites also have limitations such as '10 free downloads per day' for
freepik.com. -->
* **Splash Image:** https://www.freepik.com/free-psd/flat-lay-composition-green-leaves-with-mock-up_11434581.htm
* **Background Texture:** https://www.freepik.com/free-vector/vintage-ornamental-flowers-background_6073803.htm#page=1&query=plants%20background%20pattern&position=0
* **Icons:** https://www.freepik.com/free-vector/seedling-flat-icons-set_4368661.htm#page=1&query=plants%20icons&position=0
* **Accent art:** https://www.freepik.com/free-vector/cute-collection-cactus-watercolor_10122442.htm
* **Fake product images:** n/a


--------------------------------------------------------------------------------
## Required Seeder Data
### `users`
* demo user
* second user

### `products`
* three tree products
* three flower products
* three herb products
* a tool product

### `favorites`
* 3 favorited products for demo user



--------------------------------------------------------------------------------
## Local Setup

1. In the root directory in the terminal, `pipenv install`
2. In 'react-app' in the terminal, `npm install`
3. In postgres, create a user and database, then an `.env` file to match `.env.example` with the database credentials.
4. Migrate the data with `pipenv run flask db migrate`, `pipenv run flask db upgrade`, `pipenv run flask seed all`.
5. In the root directory n the terminal, run `flask run`.
6. In `react-app` in a separate terminal, run `npm start`
7. If not taken there automatically, check `localhost:3000` to see your life local server.



--------------------------------------------------------------------------------
## Getting started

1. Clone this repository (only this branch)

   ```bash
   git clone https://github.com/appacademy-starters/python-project-starter.git
   ```

2. Install dependencies

      ```bash
      pipenv install --dev -r dev-requirements.txt && pipenv install -r requirements.txt
      ```

3. Create a **.env** file based on the example with proper settings for your
   development environment
4. Setup your PostgreSQL user, password and database and make sure it matches your **.env** file

5. Get into your pipenv, migrate your database, seed your database, and run your flask app

   ```bash
   pipenv shell
   ```

   ```bash
   flask db upgrade
   ```

   ```bash
   flask seed all
   ```

   ```bash
   flask run
   ```

6. To run the React App in development, checkout the [README](./frontend/README.md) inside the `frontend` directory.

***
*IMPORTANT!*
   If you add any python dependencies to your pipfiles, you'll need to regenerate your requirements.txt before deployment.
   You can do this by running:

   ```bash
   pipenv lock -r > requirements.txt
   ```

*ALSO IMPORTANT!*
   psycopg2-binary MUST remain a dev dependency because you can't install it on apline-linux.
   There is a layer in the Dockerfile that will install psycopg2 (not binary) for us.
***



--------------------------------------------------------------------------------
## Deploy to Heroku

1. Create a new project on Heroku
2. Under Resources click "Find more add-ons" and add the add on called "Heroku Postgres"
3. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line)
4. Run

   ```bash
   heroku login
   ```

5. Login to the heroku container registry

   ```bash
   heroku container:login
   ```

6. Update the `REACT_APP_BASE_URL` variable in the Dockerfile.
   This should be the full URL of your Heroku app: i.e. "https://flask-react-aa.herokuapp.com"

7. Push your docker container to heroku from the root directory of your project.
   This will build the dockerfile and push the image to your heroku container registry

   ```bash
   heroku container:push web -a {NAME_OF_HEROKU_APP}
   ```

8. Release your docker container to heroku

   ```bash
   heroku container:release web -a {NAME_OF_HEROKU_APP}
   ```

9. set up your database:

   ```bash
   heroku run -a {NAME_OF_HEROKU_APP} flask db upgrade
   heroku run -a {NAME_OF_HEROKU_APP} flask seed all
   ```

10. Under Settings find "Config Vars" and add any additional/secret .env variables.

11. profit



<!-- OPTIONAL - IF YOU HAVE TESTS
--------------------------------------------------------------------------------
## Tests
1. In the root directory in the terminal, run `pytest`.
2. profit 
-->

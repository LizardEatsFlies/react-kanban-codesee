<!-- Description: A Trello-like application built with React and Redux. Take a look at the live website:  -->
Original app at: https://github.com/markusenglund/react-kanban

# An Open-Source Kanban App with CodeSee
At CodeSee, we've found this to be a great app to get up and running with CodeSee. We're hoping you will too!

## Preparing the React Kanban app
Follow this process to get the app running. **You only need to do this the very first time you get the app set up.**

Clone the repo to a local directory. Run the following command in your terminal:

```
git clone git@github.com:Codesee-io/react-kanban.git
```

Enter the new cloned directory:

```
cd react-kanban
```

Install dependencies:

```
npm install
```

> Please don’t worry that there are “14 vulnerabilities”, these will not be a problem for you running the app locally on your computer.

Build the app:

```
npm run build
```

> Please allow this command to run for a while. You’ll know it’s done when you see:
> 
> `[webpack-cli] watching files for updates...`

Now that the build is complete, we can stop the build:

    Type the key combination: <ctrl> + c

The React Kanban app should now be ready to go!

## Starting the React Kanban app
**You should do this each time you want to use the app.**

To start the app, run the following in your terminal, in the react-kanban directory:

```
npm run serve
```

> You’ll know it’s working when you see:
> `Server listening on port 1337`

You can now open your internet browser and go to http://localhost:1337 where you should see the React Kanban app, and the CodeSee purple eye.

![Screen Shot 2021-02-16 at 2 35 56 PM](https://user-images.githubusercontent.com/334845/108133912-2be1e180-706a-11eb-9cb8-8921c22477ef.png)

When you are done using the React Kanban app, you can stop the app by returning to your terminal where you previously ran `npm run serve` and using the key combination: \<ctrl\> + c

## Remember to have the CodeSee server running when making a recording!
When you’re ready to make a recording, just be sure that you have the CodeSee server running.

In a different terminal window from the React Kanban app, go to the codesee-alpha directory, and run the command:

```
docker-compose up
```

> You’ll know it’s working when you see the message:
> `node_backend_1  | server started at http://localhost:5198`


## Making your first CodeSee recording
If you have the CodeSee server running, and you see the CodeSee purple eye, you are ready to make a recording.

1. Click the recording button (the purple eye, which should change into a recording animation)
2. Interact with the React Kanban app. Remember to keep recordings as short as possible. Long recordings are difficult for the CodeSee alpha.
3. When you’re done interacting, click the recording button again. In a few moments, a new tab should pop up with the CodeSee UI.

Some things to explore:
* explore both the Overview and DataFlow tabs
  * Notice the (...) menu, and try filtering a function out, and restoring it back in.
* In the data flow tab
  * try clicking a chevron to expand a data value
  * notice as you hover over some areas, regions of the code highlight
  * try clicking the pink “dive in” buttons to see how one function calls another function
  * as you scroll, notice how headers stack along the top of the screen ー especially after clicking a few “dive in” buttons -- to help you track where you are.
  * try finding a loop (try clicking “dive in” on map() ) and dragging the loop slider to see the data change
  * In the upper-right-hand corner, click the chevron to expand the Story Side Bar. Now you can add notes for yourself, and link those notes to specific lines of code. As you explore the data flow and build an understanding, you can jot thoughts down to make it easy to remember everything you've found.




---

**Below is the original README from the React Kanban repo**


# React Kanban

A server-rendered React app inspired by [Trello](https://trello.com/home).

![react kanban example](https://github.com/yogaboll/react-kanban/blob/master/example.gif?raw=true)

[Check out the live website](https://www.reactkanban.com)

### Features

* It has most of the features available on Trello, like creating and editing new cards, dragging around cards and so on.
* Supports GitHub flavored markdown, which enables stuff like headings and checklists on the cards.
* Works great on touch devices.

### Tech stack

* [React](https://github.com/facebook/react)
* [Redux](https://github.com/reactjs/redux)
* [React-beautiful-dnd](https://github.com/atlassian/react-beautiful-dnd)
* [Sass](https://github.com/sass/sass)
* [Webpack](https://github.com/webpack/webpack)
* [Babel](https://github.com/babel/babel)
* [Express](https://github.com/expressjs/express)
* [MongoDB](https://github.com/mongodb/mongo)
* [Passport](https://github.com/jaredhanson/passport)


### Development

Setting up the full app with your own mongoDB instance and auth credentials for Twitter and Google sign-in requires significant effort. Use the simplified set up if you don't want to bother with that.

#### Simplified setup

```shell
# Clone the simple-dev branch which does not include db and social sign-in stuff
git clone https://github.com/yogaboll/react-kanban.git -b simple-dev

cd react-kanban

npm install

npm run build

# Open a second terminal window and run:
npm run serve
```

The app will run on http://127.0.0.1:1337

#### Full setup

```shell
git clone https://github.com/yogaboll/react-kanban.git

cd react-kanban

npm install
```

You need to add your own mongoDB url as well as auth credentials for the Google and Twitter sign in. You need to create a file with the name `.env` in the root directory with the following variables:

```
MONGODB_URL
MONGODB_NAME
TWITTER_API_KEY
TWITTER_API_SECRET
GOOGLE_CLIENT_ID
GOOGLE_CLIENT_SECRET
SESSION_SECRET

# Has to be port 1337
ROOT_URL=http://127.0.0.1:1337
```

```shell
npm run build
npm run serve
```

For production deployment run:

```shell
npm run build:prod
npm run serve:prod
```

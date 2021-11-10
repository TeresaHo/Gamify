# Description of Project

## Short Description of Project

This project aims at creating a hub of four different games which is meant to bring people together online. Players login with their Spotify accounts, and are redirected to a welcome page. There, they can either create their own room or join an existing room. In a room, they can invite their friends to play one of four different music-related quiz games, some of which use Spotify to play audio tracks or retrieve personal information from Spotify about the user (with their consent, of course).

## What We Have Done

- Login view, where a user can sign in using their Spotify account (not completely finished it), after which they're re-directed to:
- Welcome view, where a user can create their own room, or type in a room ID and join an existing room.
- Lobby view, which is the room's lobby. Here, users can see who else is in the room and there are 4 game options that the host of the room can select for the users in the room to play.
- Results view, the end of a game, where the player's results are shown in a descending order.
- Game view for the Music Quiz Game, where users can select one of 4 answers to a question which is displayed at the top.
- We have also created a model/backend with a database in firebase for data persistence. We also implemented calls to Spotify via their API to authenticate a user. Furthermore, we integrated the views with the model via presenters (using the MVP-model).

## What Else We Intend To Do

We intend to finish the implementation of our first game, the Music Quiz Game. After that, we will implement three more music-related games. one of which is "Do You Know Me?" where players get to answer questions about each other's music tastes (data will be retrieved from Spotify playlists/most liked songs etc) and a couple of other games.

## Project File Structure

- src/index.js: project entry point.
- src/reportWebVitals.js: setup code.
- gamify/public/\_: setup code.
- gamify/\_: setup code, gitignore, eslint & prettier for correct code styling. Config files.

* src/api/opentriviadb/opentriviadb.js: contains api calls to opentriviadb (which returns a question and 4 possible answers, one of which is correct. Used in the Music Quiz Game. also contains api
* api/spotify/spotify.js: contains api calls to spotify, currently only to authenticate the user. Will expand to also include retrieving information about user music tastes (most played songs, playlists etc) or whatever is necessary for the other games.

* src/app/app.jsx: the app itself, where routing is done etc.
* app/showPresenter.jsx: Used in app.jsx to show hashes correctly etc.

* app/gameInterface/Player.jsx: an individual player object.
* app/gameInterface/game.css: css for the game.
* app/gameInterface/resultsPresenter.jsx: presenter for the resultsView
* app/gameInterface/resultsView: View showing the results of a game

* app/homepage/welcomeView: view of the welcome page (the one user is redirected to after logging in.
* app/homepage/welcomePresenter: presenter of the welcomeView.
* app/homepage/createPresenter.jsx: depending on the state, shows either a game or a join view (the lobby of a room).
* app/homepage/gamePresenter.jsx: shows either the lobby of a room or the game view, depending on current state.
* app/homepage/game.css: css styling.

* app/lobby/lobbyview.jsx: The lobby view of a room.
* app/lobby/lobbyPresenter.jsx: presenter of lobby view.
* app/lobby/lobby.css: css styling for the lobby.

* app/login/loginView.jsx: login view.
* app/login/loginPresenter.jsx: presenter of login view.
* app/login/login.css: css styling for login page.

* app/reusable_components/choiceButton/choiceButtonView.jsx: the view for a choice button, consider it a button component.
* app/reusable_components/choiceButton/choiceButton.css: css styling of button component.
* app/reusable_components/game/gamePresenter.jsx: the presenter of a game, which shows a question and choice buttons.
* app/reusable_components/game/questionView.jsx: shows a game question.

* src/assets/css/global.css: global css styling used by different views.
* assets/fonts/\_: fonts.
* assets/images/\_: images.

* src/data/firebase/firebase.js: communicating with firebase and modifying the database.
* data/firebase/firebaseUtils.js: communicating with firebase and modifying the database.
* data/model/model.js: a class which each connected user instantiates, with their unique information (such as which roomID they're in, their login tokens etc).
* data/model/message.js: to send data from the model to the observers.

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

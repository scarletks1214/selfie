This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Architecture

The Selfies has 2 pages - Camera page and Gallery Page

Camera page has react camera component, auth buttons and gallery button.

Gallery page has a menu for generating gif files.

The src folder is consist of container, components, config, utils and assets folders.

'config' folder includes sort of settings info of the app while 'utils' folder includes apis functions to google drive and image utilities. 'containers' and 'components' folder includes components for pages, camera and gallery item components. 'assets' folder has an image - logo.png.

### How the app is built

components/CameraScreen component uses [react-html5-camera-photo](https://www.npmjs.com/package/react-html5-camera-photo) package to take a picture with front-facing camera.
Captured image can be saved as a jpg file on google drive or local according to logged in state.

[file-saver](https://www.npmjs.com/package/file-saver) package is used to create image file from base64 code.
The prefix of the saved image name has created date.(e.g. Selfie-2019-5-20-1558264796101.jpg)

[Google APIs](https://developers.google.com/drive/api/v3/about-files) are used to create folder, fetch images and upload images to google drive.

[gifshot](https://www.npmjs.com/package/gifshot) package is used to generating gif file from image list

User can select images that are necessary to create gif file in the gallery page.

User can select gif width with small/medium/large options.

The width of gif is set in src/config/config-global.js

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify

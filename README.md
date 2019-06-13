This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Architecture

1. Authentication

User signs in the app with google account in the first page.

2. Taking a picture

User can take a picture and store it.
If signed-in user takes a picture, it is uploaded to 'Selfie-Webapp' folder in google drive.
If non-signed in user takes a picture, it is stored in local.

3. View taken pictures and gif generation

Signed-in user can see taken pictures.

User can see all the taken pictures from the 'Selfie-Webapp' folder of google drive.
User can generate a gif file made up of them. User can also choose one gif size of small/medium/large options. The generated gif file is downloaded to local.

4. Pages hierarchy

This app consists of 2 pages - Camera page and Gallery Page.

### How the app is built

This web app is built with create-react-app.

It uses browser API called getUserMedia to access device camera and take a picture.

It uses Google API to login and store pictures to google drive.

This app uses [code spliting](https://reactjs.org/docs/code-splitting.html) for performance optimization.

It is deployed to [https://selfie-everyday-app.firebaseapp.com](https://selfie-everyday-app.firebaseapp.com)

### `Camera Page`

The first page consists of front-facing camera screen, login/out buttons, and gallery button.

Taken pictures are saved as jpg on google drive or local according to logged-in state.

[Google APIs](https://developers.google.com/drive/api/v3/about-auth) are used to login with google account

[react-html5-camera-photo](https://www.npmjs.com/package/react-html5-camera-photo) package is used to take a picture with a front-facing camera.

[file-saver](https://www.npmjs.com/package/file-saver) package is used to create an image file from base64 code.

### `Gallery Page`

The second page(gallery) includes gif generating menu and pictures gallery that shows taken pictures in 'Sefie-Webapp' folder of google drive.

User can select pictures for generating a gif file.

User can choose one gif width of small/medium/large options.

[Google APIs](https://developers.google.com/drive/api/v3/about-files) are used to create a folder inside, fetch pictures from, and upload pictures to google drive.

[gifshot](https://www.npmjs.com/package/gifshot) package is used to generate gif file from the selected pictures

### `Folder structure`

The src folder mainly consists of container, components, config, and utils subfolders.

'config' folder includes sort of settings info of the app while 'utils' folder includes API functions to access google drive and image manipulation utilities. 'containers' and 'components' folder includes components.

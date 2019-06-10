### Architecture

User signs in the app with google account in the first page.

If signed in user takes a picture, it is uploaded to 'Selfie-Webapp' folder in google drive.
If non-signed in user takes a picture, it is downloaded to local.

Signed in user can see his pictures in the gallery page.

The gallery page shows all the images in the 'Selfie-Webapp' folder of google drive.
Each gallery item is selectable and the user can generate a gif file with selected images.
User can select the gif size with small/medium/large option.
A generated gif file is downloaded to local.

The Selfies has 2 pages - Camera page and Gallery Page

Camera page has camera component, auth buttons, and gallery button.

The gallery page has a menu for generating gif files.

### How the app is built

This web app is built with create-react-app. Webcam is required to take a picture.

It uses react-html5-camera-photo and some material ui components for UI.
The project uses [code spliting](https://reactjs.org/docs/code-splitting.html) for performance optimization.

This app is deployed to [firebase](https://selfie-everyday-app.firebaseapp.com/)

### `First Page`

The first page includes google login/out buttons, camera, and gallery button.
The taken picture can be saved as a jpg file on google drive or local according to logged in state.

[Google APIs](https://developers.google.com/drive/api/v3/about-auth) are used to login with google account

[react-html5-camera-photo](https://www.npmjs.com/package/react-html5-camera-photo) package is used to take a picture with a front-facing camera.

[file-saver](https://www.npmjs.com/package/file-saver) package is used to create an image file from the base64 code.
The prefix of the saved image name has created date.(e.g. Selfie-2019-5-20-1558264796101.jpg)

### `Gallery Page`

The second page(gallery) includes gif generating menu and a gallery that shows images in 'Sefie-Webapp' folder of google drive.

User can select images that are necessary to create a gif file in the gallery page.

User can select gif width with small/medium/large options.

[Google APIs](https://developers.google.com/drive/api/v3/about-files) are used to create a folder, fetch images, and upload images to google drive.

[gifshot](https://www.npmjs.com/package/gifshot) package is used to generate gif file from the selected image list

### `Folder structure`

The src folder mainly consists of container, components, config, and utils subfolders.

'config' folder includes sort of settings info of the app while 'utils' folder includes apis functions to google drive and image utilities. 'containers' and 'components' folder includes components for pages, camera, and gallery item components.


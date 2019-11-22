# React Application

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

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

## Docker

### Development and Testing Environments

1. Run the `docker-compose.yaml` file in the detached mode, as follows:

   ```shell
   docker-compose up -d .
   ```

2. Open your browser and navigate to [http://localhost:3000](http://localhost:3000) to see the application running.

3. You can see the results of running the test suites as follows:

   ```shell
   docker container logs <container_id> .
   ```

   *Note*: Replace <container_id> with the container id of the testing environment

4. After finishing, shut down all the running containers, as follows:

   ```shell
   docker-compose down
   ```

### Production Environment

1. Build the `Dockerfile.prod` and get the image id, as follows:

   ```shell
   docker build -f Dockerfile.prod .
   ```

2. Run a container from the generated image with a port mapping flag, as follows:

   ```shell
   docker container run -p 80:80 <image_id>
   ```

   *Note*: Replace <image_id> with a real image id

3. Open your browser and navigate to [http://localhost](http://localhost) to see the application running.

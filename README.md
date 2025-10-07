
# Placement Assistant Bot

This project is a Placement Assistant Bot with a React frontend and a FastAPI backend. It helps students with placement-related queries using verified data and a local Llama language model.

## Features
- React-based chat frontend
- FastAPI backend with semantic search and Llama LLM fallback
- Uses local Llama model for natural language answers
- Placement data stored in CSV and indexed with FAISS

---

## Setup Instructions

### 1. Prerequisites
- **Python 3.10+** (for backend)
- **Node.js 16+** (for frontend)
- **Ollama** (for running Llama models locally)

### 2. Backend Setup
1. Navigate to the `backend` directory:
	```sh
	cd backend
	```
2. Install Python dependencies:
	```sh
	pip install -r requirements.txt
	```
3. Download and install Ollama from [https://ollama.com/](https://ollama.com/).
4. Pull the Llama model (e.g., llama3):
	```sh
	ollama pull llama3
	```
5. Start the Ollama server (if not already running):
	```sh
	ollama serve
	```
6. Make sure the Llama model is available at the path specified in `app.py` (default: `backend/model/llama-3.2`). Adjust the path if needed.
7. Run the FastAPI server:
	```sh
	uvicorn app:app --reload
	```

### 3. Frontend Setup
1. Navigate to the `frontend` directory:
	```sh
	cd frontend
	```
2. Install dependencies:
	```sh
	npm install
	```
3. Start the React app:
	```sh
	npm start
	```

---

## Notes
- The backend requires a running Ollama server with the Llama model installed.
- If you change the Llama model or its path, update `LLAMA_MODEL_PATH` in `backend/app.py`.
- Placement data is loaded from `backend/placement_data.csv`.

---

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

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

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

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

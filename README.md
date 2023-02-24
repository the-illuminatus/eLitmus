
<p align="left">
  Assesment Proctoring Tool.
</p>

### Contents

- [Steps](#steps)
- [Design](#design)
- [Technologies Used](#technologies-used)
- [Authors](#authors)


* Problem Statement

eLitmus is a recruitment and assessment company that conducts tests across the globe. One of the most common challenges we face is preventing cheating during exams. We need your help to design and create a chrome extension to address this issue.

A Chrome extension that operates on assessment websites, activating when a user opens a test page. It opens a form for the user to enter their name, email, and test invitation code, and upon clicking the "Start Test" button, the user's information is sent to the backend server for storage. The extension performs a camera and audio check, and initiates image proctoring, sending images to the server every three minutes (configurable). All image and user activity data are stored on the backend server.

AIM to develop an application that can automatically proctor and monitor students, without the need of manual proctoring - ie without a teacher's aid.
That's where we come into picture.

## Steps

* To Create the frontend of the extension using HTML, CSS, and JavaScript. You can use a JavaScript framework like React or Vue.js to simplify the development process. Create a form for the user to enter their name, email, and test invitation code. Add a "Start Test" button to the form that triggers the submission of the form data to the backend server.
* To Add a webcam and microphone check to the extension. Use the getUserMedia API to access the user's camera and microphone and check if they are working properly. You can use a library like RecordRTC to capture video and audio data.
* To Implement the image proctoring functionality by using a setInterval function to capture screenshots of the user's browser every three minutes (or any other configurable interval). You can use a library like html2canvas to capture screenshots.
* To Create a backend server using a server-side programming language like Node.js or Python. Use a database like MongoDB or MySQL to store the user information and images. You can also use cloud-based storage services like Amazon S3 or Google Cloud Storage to store the images.
* To Create a RESTful API that allows the extension to submit user information and images to the backend server. The API should store the information in the database and store the images in the cloud storage service.
* To Create an admin dashboard that displays all the user information and stored images. You can use a web-based dashboard framework like Bootstrap or Materialize to create the dashboard.


* Architecture

- The architecture and workflow was built using [excalidraw](https://excalidraw.com).

### Design

- The designs were built using [Figma](figma.com) and were brought to life with [React](https://beta.reactjs.org).

**Register & Login**
<br />

<table>
    <tr>
        <td>
          <p>User Registration - Face Verifacation to be done when exam starts.</p>
        </td>
        <td>
          <p>User Login to start the exam.</p>
        </td>
    </tr>
</table>



**Creating a Test and Dashbaord**

<br />

<table>
    <tr>
        <td>
          <p>Creating a test and expecting a Google/Microsoft Form Link</p>
        </td>
        <td>
          <p>Admin Dashboard: Tests arranged chronologically.</p>
        </td>
    </tr>
</table>

**Start Exam**

- After logging in and entering the unique test code.
- Live Snapshots will be captured, periodically and will be analysed for the following :
  -  Face Verification
  -  Face Cover/Visibility
  -  Multiple People Detection


**Checks for cheating**

- Face Verification
- Voice Detection
- Multiple Tabs Check
- Full Screen Check


**Test Admin Dashboard**

- The following warning logs, data and statistics will be emailed to the Admin after the test.

<br />

<table>
    <tr>
        <td>
          <p>Test Dashboard: Admin can see statistics - no. of students with warnings and above the threshold.</p>
        </td>
        <td>
          <p>Admin Dashboard: Admin can Terminate or Continue a students exam based on warnings.</p>
        </td>
    </tr>
</table>


<br />

## Technologies Used



- Prototyping and Frontend Design
  - Figma
- Frontend
  - React.js
  - CSS
- Backend
  - Node.js (Express.js)
  - MongoDB
- Machine Learning
  - OpenCV
  - Flask


**Dependencies**

A freaking huge shoutout to:
- [react-webcam](https://www.npmjs.com/package/react-webcam)
- [devtools-detect](https://www.npmjs.com/package/devtools-detect)
- [react-chartjs-2](https://www.npmjs.com/package/react-chartjs-2)
- [chartjs](https://www.npmjs.com/package/chartjs)

**Project Structure**
- The project contains 4 broad directories.

```
*
├───client
├───extension
├───model
└───server
```

- `client`: The frontend for the application.
- `extension`: Chrome/Edge extension to keep a track of browser tabs.
- `model`: Model APIs for Machine Learning.
- `server`: The backend for the application.



**Client**

For local setup of frontend:
- `cd client`
- `npm i`
- `npm start`
- Go to `localhost:3000`

Structure

```
src
├───assets
├───components
├───containers
└───index.js
```

Individual Component & Container Structure

```
component
├───component.jsx
└───component.css
```

**Server**

For local setup of backend:
- `cd server`
- `npm i`
- `npm start`

```
server
├───controllers
├───middlewares
├───models
├───routes
└───package.json
```

<br />


### Authors

- Sujit Bhalekar 
  - [LinkedIn](https://www.linkedin.com/in/sujit-bhalekar-28bba4206/)


<!DOCTYPE html>

<html lang="en">

<head>

 <meta charset="UTF-8">

 <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>Array Operations: Append Object and Check if Array</title>

</head>

<body>
<h1>Append Object to Array & Check if an Object is an Array</h1>

 <div class="form-section">

 <h3>Append an Object to Array</h3>

 <label for="objectKey">Enter Key: </label>

 <input type="text" id="objectKey" placeholder="Enter object key">

 <label for="objectValue">Enter Value: </label>

 <input type="text" id="objectValue" placeholder="Enter object value">

 <button onclick="appendObject()">Append Object</button>

 <p><strong>Array:</strong> <span id="arrayDisplay">[]</span></p>

 </div>

 <div class="form-section">

 <h3>Check if an Object is an Array</h3>

 <button onclick="checkIfArray()">Check</button>

 <p id="checkResult"></p>

 </div>

 <script> let array = []; // Initial empty array

 function appendObject() {

 const key = document.getElementById('objectKey').value;

 const value = document.getElementById('objectValue').value;

 if (key && value) {
   const newObject = {};

 newObject[key] = value; // Create a new object with the entered key-value pair

 array.push(newObject); // Append the object to the array

 displayArray();

 document.getElementById('objectKey').value = ''; // Clear input fields

 document.getElementById('objectValue').value = '';

 }

}

// Function to display the array

function displayArray() {

 document.getElementById('arrayDisplay').innerText = JSON.stringify(array);

}

// Function to check if the array variable is an array

function checkIfArray() {

 const result = Array.isArray(array);

 document.getElementById('checkResult').innerText = result ? "Yes, it's an array." : "No, it's 

not an array.";

}

</script>

</body>

</html>
 

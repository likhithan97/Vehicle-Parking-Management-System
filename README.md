# Vehicle-Parking-Management-System
A vehicle parking management system that helps to manage parking spaces, track vehicles, and improve efficiency.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2d037966-c265-40f3-9f92-40004aaa451b" />
<!DOCTYPE html>
<html>
<head>
    <title>Vehicle Parking Management System</title>
    <style>
        body {
            font-family: Arial;
            background-color: #f2f2f2;
            text-align: center;
        }
        h1 {
            background-color: #333;
            color: white;
            padding: 10px;
        }
        .container {
            margin-top: 30px;
        }
        input, select {
            padding: 10px;
            margin: 10px;
            width: 200px;
        }
        button {
            padding: 10px 20px;
            background-color: green;
            color: white;
            border: none;
            cursor: pointer;
        }
        table {
            margin: 20px auto;
            border-collapse: collapse;
            width: 60%;
        }
        table, th, td {
            border: 1px solid black;
        }
        th, td {
            padding: 10px;
        }
    </style>
</head>
<body>

<h1>Vehicle Parking Management System</h1>

<div class="container">
    <input type="text" id="owner" placeholder="Owner Name">
    <input type="text" id="vehicle" placeholder="Vehicle Number">
    
    <select id="type">
        <option value="">Select Vehicle Type</option>
        <option>Bike</option>
        <option>Car</option>
    </select>
    
    <button onclick="addVehicle()">Park Vehicle</button>
</div>

<table id="parkingTable">
    <tr>
        <th>Owner Name</th>
        <th>Vehicle Number</th>
        <th>Type</th>
        <th>Status</th>
    </tr>
</table>

<script>
    function addVehicle() {
        let owner = document.getElementById("owner").value;
        let vehicle = document.getElementById("vehicle").value;
        let type = document.getElementById("type").value;

        if(owner === "" || vehicle === "" || type === "") {
            alert("Please fill all details");
            return;
        }

        let table = document.getElementById("parkingTable");
        let row = table.insertRow();

        row.insertCell(0).innerHTML = owner;
        row.insertCell(1).innerHTML = vehicle;
        row.insertCell(2).innerHTML = type;
        row.insertCell(3).innerHTML = "Parked";

        document.getElementById("owner").value = "";
        document.getElementById("vehicle").value = "";
        document.getElementById("type").value = "";
    }
</script>

</body>
</html>

# Figma-Project
Project Related Athelet Health Report


<!DOCTYPE html>
<html>
<head>
	<title>Athlete Health Dashboard</title>
	<link rel="stylesheet" href="style.css">
	<script src="Athelet.js"></script>
    <style>

        body
        {
            background-color: silver;
        }

        table
         {
	border-collapse:separate;
	width: 100%;
    
}

th, td {
	text-align: left;
	padding: 8px;
    /* background-color:aliceblue; */
}

th {
	background-color: grey;
}

tr {
	 background-color: snow;
}

tr:hover {
	background-color:aqua;
	cursor: pointer;
}

#health-report {
	display: none;
}

#health-report img {
	width: 100%;
}

#health-report h2 {
	margin-top: 30px;
}

#health-report p {
	margin-top: 10px;
}

    </style>
</head>
<body>
	<h1 style="text-align: center;">Athlete Health Dashboard</h1>
	<table id="athlete-list">
		<thead>
			<tr>
				<th>Personal ID</th>
				<th>Name</th>
				<th>Email</th>
				<th>Report</th>
			</tr>
            <!-- <tr>
                <td>1</td>
                <td>John Doe</td>
                <td>johndoe@example.com</td>
                <td><a href="Athlete.json"></a>Athlete1_Report</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Jane Smith</td>
                <td>janesmith@example.com</td>
                <td>Athlete2_Report</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Bob Johnson</td>
                <td>bobjohnson@example.com</td>
                <td>Athlete3_Report</td>
            </tr> -->

		</thead>
		<tbody>
			<!-- Add athlete details here -->
		</tbody>
	</table>
	<div id="health-report">
		<!-- Health report details will be displayed here -->
	</div>
    <script>
        //Define athlete details
    const athletes = [
        {
            id: 1,
            name: 'John Doe',
            email: 'johndoe@example.com',
            report: 'Report'
        },
        {
            id: 2,
            name: 'Jane Smith',
            email: 'janesmith@example.com',
            report: 'report2.json'
        },
        {
            id: 3,
            name: 'Bob Johnson',
            email: 'bobjohnson@example.com',
            report: 'report3.json'
        }
    ];
    
    // Populate athlete list
    const athleteList = document.querySelector('#athlete-list tbody');
    athletes.forEach((athlete) => {
        const row = document.createElement('tr');
        row.innerHTML = `
            <td>${athlete.id}</td>
            <td>${athlete.name}</td>
            <td>${athlete.email}</td>
            <td>${athlete.report}</td>
        `;
        row.addEventListener('click', () => {
            loadHealthReport(athlete.report);
        });
        athleteList.appendChild(row);
    });
    
    //Load health report
    function loadHealthReport(reportFile) {
        const healthReport = document.querySelector('#health-report');
        healthReport.innerHTML = '';
        healthReport.style.display = 'block';
        const img = document.createElement('img');
        img.src = 'E:\Club_Health_Dashboard\brain.png'; // replace with your own image file
        healthReport.appendChild(img);
        const h2 = document.createElement('h2');
        h2.textContent = 'Whole Brain Volume';
        healthReport.appendChild(h2);
        const p = document.createElement('p');
        p.textContent = 'Distribution plot of whole brain volume.';
        healthReport.appendChild(p);
       // Use CSV data to create distribution plot
    }
    
    </script>
</body>
</html>




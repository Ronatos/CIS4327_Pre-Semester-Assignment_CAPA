// VER 0.1X in real scenario sql database is already established, this is only for simplicity sake
var mysql = require('mysql');

var con = mysql.createConnection({
	host: "localhost",
	user: "user",
	password: "password",
	database: "testdb"
});

con.connect(function (err) {
	if (err) throw err;
	console.log("Connected!");
	var sql = "CREATE TABLE opportunities (opt_name varchar(20), available varchar(3), grade char(1) primary key(dept_name))";
	con.query(sql, function (err, result) {
		if (err) throw err;
		console.log("Table created");

	});
	var sql = "INSERT INTO opportunities (opt_name, available, grade) VALUES ?";
	var values = [
		['ExampleOpp1', 'Yes', 'A'],
		['ExampleOpp2', 'No', 'A'],
		['ExampleOpp3', 'Yes', 'C'],
	];
	con.query(sql, [values], function (err, result) {
		if (err) throw err;
		console.log("Number of records inserted: " + result.affectedRows);
	});

	/*TO DOs
	 SQL Database will be read from and written into a Table (which includes an edit button)
	 Create Search filter event listener
	 No Filter will display entire table
	
	if no opportunites match system displays no matches


	opportunties presented have "View Volunteer Opportunity Matches Option"
	which will display matches volunteers (volunteers are graded and matched with potential opportunites A-F scale for simplicity)

	create filter for volunteer search and display

	in the event an error occurs during an edit user is asked to reenter info

	add new opportunity within the table and display

	delete opportunity option
	refresh to show information
	*/
});

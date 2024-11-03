<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Live Poll: Is Orestas Gay?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .poll-container {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        button {
            padding: 10px 20px;
            margin: 5px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            background-color: #007bff;
            color: white;
        }
        button:hover {
            background-color: #0056b3;
        }
        #result {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="poll-container">
        <h1>Is Orestas Gay?</h1>
        <button onclick="vote('yes')">Yes</button>
        <button onclick="vote('no')">No</button>
        <div id="result"></div>
    </div>

    <script>
        let yesVotes = 0;
        let noVotes = 0;

        function vote(option) {
            if (option === 'yes') {
                yesVotes++;
            } else {
                noVotes++;
            }
            displayResults();
        }

        function displayResults() {
            const totalVotes = yesVotes + noVotes;
            const yesPercentage = totalVotes > 0 ? (yesVotes / totalVotes * 100).toFixed(2) : 0;
            const noPercentage = totalVotes > 0 ? (noVotes / totalVotes * 100).toFixed(2) : 0;

            document.getElementById('result').innerHTML = `
                <h2>Results:</h2>
                <p>Yes: ${yesVotes} votes (${yesPercentage}%)</p>
                <p>No: ${noVotes} votes (${noPercentage}%)</p>
            `;
        }
    </script>
</body>
</html>

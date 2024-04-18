
```html
<!DOCTYPE html>
<html>
<head>
    <title>Student Union Election</title>
    <style>
        /* Basic CSS for styling */
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        header {
            text-align: center;
            margin-bottom: 20px;
        }
        .candidate-list {
            list-style-type: none;
            padding: 0;
        }
        .candidate-item {
            border: 1px solid #ccc;
            margin-bottom: 10px;
            padding: 10px;
            display: flex;
            align-items: center;
        }
        .candidate-item img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 10px;
        }
        .candidate-item label {
            flex-grow: 1;
        }
        button {
            display: block;
            width: 100px;
            margin: 20px auto;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <header>
        <h1>Student Union Election</h1>
        <p>Choose your candidate for president.</p>
    </header>
    
    <form id="election-form">
        <ul class="candidate-list">
            <li class="candidate-item">
                <input type="radio" id="candidate1" name="candidate" value="candidate1">
                <label for="candidate1">
                    <img src="candidate1.jpg" alt="Candidate 1">
                    Candidate 1
                </label>
            </li>
            <li class="candidate-item">
                <input type="radio" id="candidate2" name="candidate" value="candidate2">
                <label for="candidate2">
                    <img src="candidate2.jpg" alt="Candidate 2">
                    Candidate 2
                </label>
            </li>
            <li class="candidate-item">
                <input type="radio" id="candidate3" name="candidate" value="candidate3">
                <label for="candidate3">
                    <img src="candidate3.jpg" alt="Candidate 3">
                    Candidate 3
                </label>
            </li>
            <!-- Add more candidates as needed -->
        </ul>
        
        <button type="submit">Submit Vote</button>
    </form>

    <script>
        // Script to handle form submission
        document.getElementById('election-form').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent form from submitting the default way
            
            const formData = new FormData(event.target);
            const selectedCandidate = formData.get('candidate');
            
            if (selectedCandidate) {
                alert(`You have voted for ${selectedCandidate}`);
                // Handle form submission here (e.g., send data to server)
            } else {
                alert('Please select a candidate before submitting your vote.');
            }
        });
    </script>
</body>
</html>

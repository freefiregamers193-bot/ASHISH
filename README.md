<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GGSIPU Examination Division - Student Portal</title>
    <style>
        * {
            box-sizing: border-box;
        }
        body {
            font-family: Arial, Helvetica, sans-serif;
            background-color: #f5f5f5;
            margin: 0;
            padding: 0;
            color: #333;
            line-height: 1.6;
        }
        .header {
            background-color: #003087;
            color: white;
            text-align: center;
            padding: 1.5rem 1rem;
        }
        .header h1 {
            margin: 0;
            font-size: clamp(1.6rem, 5vw, 2.2rem);
        }
        .header p {
            margin: 0.3rem 0 0;
            font-size: clamp(0.9rem, 3.5vw, 1.1rem);
        }
        .container {
            max-width: 550px;
            margin: 2rem auto;
            background: white;
            padding: 2rem;
            border: 1px solid #ccc;
            border-radius: 8px;
            box-shadow: 0 2px 12px rgba(0,0,0,0.1);
            text-align: center;
        }
        .logo {
            max-width: 180px;
            height: auto;
            margin-bottom: 1.5rem;
        }
        .form-group {
            margin: 1.5rem 0;
            text-align: left;
        }
        label {
            display: block;
            margin-bottom: 0.6rem;
            font-weight: bold;
            font-size: 1rem;
        }
        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 0.9rem;
            border: 1px solid #999;
            border-radius: 4px;
            font-size: 1rem;
        }
        .captcha {
            margin: 1.5rem 0;
            text-align: center;
        }
        .captcha img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ccc;
            margin-bottom: 0.8rem;
        }
        .refresh {
            color: #003087;
            cursor: pointer;
            font-size: 0.95rem;
        }
        button {
            background-color: #003087;
            color: white;
            border: none;
            padding: 0.9rem 2.5rem;
            font-size: 1.1rem;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 1rem;
            width: 100%;
            max-width: 300px;
        }
        button:hover {
            background-color: #002060;
        }
        .forgot {
            margin-top: 1.2rem;
            font-size: 0.95rem;
        }
        .forgot a {
            color: #003087;
            text-decoration: none;
        }
        .result {
            display: none;
            max-width: 900px;
            margin: 2rem auto;
            background: white;
            padding: 2rem;
            border: 1px solid #ccc;
            border-radius: 8px;
        }
        .result h2 {
            color: #003087;
            text-align: center;
            font-size: clamp(1.4rem, 4.5vw, 1.8rem);
        }
        .result p {
            margin: 0.6rem 0;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.5rem 0;
            font-size: 0.95rem;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 0.9rem;
            text-align: left;
        }
        th {
            background-color: #e6f0ff;
            color: #003087;
        }
        .pass {
            color: green;
            font-weight: bold;
        }
        .center {
            text-align: center;
        }

        /* Responsive Table for small screens */
        @media screen and (max-width: 600px) {
            table, thead, tbody, th, td, tr {
                display: block;
            }
            thead tr {
                position: absolute;
                top: -9999px;
                left: -9999px;
            }
            tr {
                margin-bottom: 1rem;
                border: 1px solid #ddd;
                border-radius: 6px;
            }
            td {
                border: none;
                border-bottom: 1px solid #eee;
                position: relative;
                padding-left: 50%;
            }
            td:before {
                position: absolute;
                top: 0.9rem;
                left: 0.9rem;
                width: 45%;
                padding-right: 1rem;
                white-space: nowrap;
                content: attr(data-label);
                font-weight: bold;
                color: #003087;
            }
            .container, .result {
                margin: 1rem;
                padding: 1.5rem;
            }
            button {
                padding: 1rem;
                font-size: 1.1rem;
            }
        }

        @media screen and (max-width: 400px) {
            .header {
                padding: 1rem 0.8rem;
            }
            .container {
                padding: 1.2rem;
            }
        }
    </style>
</head>
<body>

<div class="header">
    <h1>Guru Gobind Singh Indraprastha University</h1>
    <p>Dwarka Sector 16-C, New Delhi - 110078</p>
    <p>Examination Division</p>
</div>

<div class="container" id="loginDiv">
    <img src="https://via.placeholder.com/180x80?text=GGSIPU+Logo" alt="GGSIPU Logo" class="logo">
    
    <h2>Student Login</h2>
    
    <div class="form-group">
        <label for="roll">User Name (Enrollment No / Roll No)</label>
        <input type="text" id="roll" placeholder="Enter your Roll Number" maxlength="11">
    </div>
    
    <div class="form-group">
        <label for="pass">Password</label>
        <input type="password" id="pass" placeholder="Enter your Password">
    </div>
    
    <div class="captcha">
        <label>Security Check</label>
        <img src="https://via.placeholder.com/200x60?text=Captcha+Here+(12345)" alt="Captcha">
        <div class="refresh">↻ Refresh</div>
    </div>
    
    <button onclick="checkResult()">Submit</button>
    
    <div class="forgot">
        <a href="#">Forgot Password?</a>
    </div>
</div>

<div class="result" id="resultDiv">
    <h2>1st Semester Examination Result</h2>
    <p class="center"><strong>Program:</strong> B.Tech (Electrical & Electronics Engineering)</p>
    <p><strong>Name:</strong> ASHISH KUMAR</p>
    <p><strong>Father's Name:</strong> BRIJESH KUMAR</p>
    <p><strong>College:</strong> MAHARAJA AGRASEN INSTITUTE OF TECHNOLOGY</p>
    <p><strong>Roll No:</strong> 25038194824</p>
    <p><strong>Exam Month/Year:</strong> Dec 2025</p>

    <table>
        <tr>
            <th data-label="Subject Code">Subject Code</th>
            <th data-label="Subject Name">Subject Name</th>
            <th data-label="Internal">Internal</th>
            <th data-label="External">External</th>
            <th data-label="Total">Total</th>
            <th data-label="Max">Max</th>
            <th data-label="Status">Status</th>
        </tr>
        <tr>
            <td data-label="Subject Code">ETMA-101</td>
            <td data-label="Subject Name">Applied Mathematics - I</td>
            <td data-label="Internal">28</td>
            <td data-label="External">54</td>
            <td data-label="Total">82</td>
            <td data-label="Max">100</td>
            <td data-label="Status" class="pass">Pass</td>
        </tr>
        <tr>
            <td data-label="Subject Code">ETPH-103</td>
            <td data-label="Subject Name">Applied Physics - I</td>
            <td data-label="Internal">26</td>
            <td data-label="External">52</td>
            <td data-label="Total">78</td>
            <td data-label="Max">100</td>
            <td data-label="Status" class="pass">Pass</td>
        </tr>
        <tr>
            <td data-label="Subject Code">ETME-105</td>
            <td data-label="Subject Name">Manufacturing Processes</td>
            <td data-label="Internal">30</td>
            <td data-label="External">55</td>
            <td data-label="Total">85</td>
            <td data-label="Max">100</td>
            <td data-label="Status" class="pass">Pass</td>
        </tr>
        <tr>
            <td data-label="Subject Code">ETEE-107</td>
            <td data-label="Subject Name">Electrical Technology</td>
            <td data-label="Internal">32</td>
            <td data-label="External">56</td>
            <td data-label="Total">88</td>
            <td data-label="Max">100</td>
            <td data-label="Status" class="pass">Pass</td>
        </tr>
        <tr>
            <td data-label="Subject Code">ETCH-113</td>
            <td data-label="Subject Name">Applied Chemistry</td>
            <td data-label="Internal">27</td>
            <td data-label="External">52</td>
            <td data-label="Total">79</td>
            <td data-label="Max">100</td>
            <td data-label="Status" class="pass">Pass</td>
        </tr>
        <tr>
            <td data-label="Subject Code">ETCS-111</td>
            <td data-label="Subject Name">Fundamentals of Computing</td>
            <td data-label="Internal">33</td>
            <td data-label="External">58</td>
            <td data-label="Total">91</td>
            <td data-label="Max">100</td>
            <td data-label="Status" class="pass">Pass</td>
        </tr>
        <tr>
            <td colspan="4" class="center" data-label="Total"><strong>Total</strong></td>
            <td data-label="Total"><strong>503</strong></td>
            <td data-label="Max"><strong>600</strong></td>
            <td data-label="Status"><strong class="pass">PASS (83.83%)</strong></td>
        </tr>
    </table>

    <p class="center" style="font-size:1.3em; color:green; margin-top:2rem; font-weight:bold;">
      ELIGIBLE FOR NEXT SEMESTER
    </p>
</div>

<script>
    function checkResult() {
        const roll = document.getElementById("roll").value.trim();
        const pass = document.getElementById("pass").value.trim();

        if (roll === "25038194824" && pass === "24072007") {
            document.getElementById("loginDiv").style.display = "none";
            document.getElementById("resultDiv").style.display = "block";
        } else {
            alert("Invalid User Name or Password. Please try again.");
        }
    }
</script>

</body>
</html>

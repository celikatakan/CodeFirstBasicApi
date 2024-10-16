<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
        }
        h2 {
            color: #555;
        }
        ul {
            line-height: 1.6;
        }
        pre {
            background-color: #f8f8f8;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Code First Approach with Entity Framework Core</h1>
        <p>This project demonstrates the Code First approach for creating a database using Entity Framework Core.</p>

        <h2>Database Context: <code>PatikaFirstDbContext</code></h2>
        <p>The database context used in this project is named <strong>PatikaFirstDbContext</strong>. The database name is <strong>PatikaCodeFirstDb1</strong>.</p>

        <h2>Database Tables</h2>
        <ul>
            <li><strong>Movies Table:</strong></li>
            <ul>
                <li><code>Id (int)</code> - Primary key, auto-incremented</li>
                <li><code>Title (string)</code> - Movie title</li>
                <li><code>Genre (string)</code> - Movie genre (e.g., Action, Comedy, Drama)</li>
                <li><code>ReleaseYear (int)</code> - Release year of the movie</li>
            </ul>

            <li><strong>Games Table:</strong></li>
            <ul>
                <li><code>Id (int)</code> - Primary key, auto-incremented</li>
                <li><code>Name (string)</code> - Game name</li>
                <li><code>Platform (string)</code> - Platform (e.g., PC, PlayStation, Xbox)</li>
                <li><code>Rating (decimal)</code> - Game rating (0 to 10)</li>
            </ul>
        </ul>

        <h2>How to Run</h2>
        <pre>
1. Clone the repository.
2. Install Entity Framework Core.
3. Run the migration commands to create the database.
        </pre>
    </div>
</body>
</html>

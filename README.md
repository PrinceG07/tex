<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XML File Loader</title>
</head>
<body>

<h2>XML File Loader</h2>

<?php
$xml = simplexml_load_file('1.xml');

if ($xml) {
   
       echo "<h3>Book Information:</h3>";

    foreach ($xml->book as $book) {
        echo "Title: " . $book->title . "<br>";
        echo "Author: " . $book->author . "<br>";
        echo "Price: $" . $book->price . "<br><br>";
    }
} else {
    echo "<p>Error loading XML file.</p>";
}
?>
</body>
</html>

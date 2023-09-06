<!DOCTYPE html>
<html>
<head>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        p {
            margin: 10px 0;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 3px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        span {
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>19</h1>

    <p>Podaj dwie liczby do dodania:</p>
    
    <input type="text" id="liczbaA" placeholder="Liczba A">
    <input type="text" id="liczbaB" placeholder="Liczba B">
    <button onclick="dodajLiczby()">Dodaj</button>
    
    <p>Wynik: <span id="wynik"></span></p>
    <p>Działanie: <span id="dzialanie"></span></p>
    <p>Wynik jest parzysty: <span id="czyParzysty"></span></p>

    <script>
        function dodajLiczby() {
            var liczbaA = parseFloat(document.getElementById("liczbaA").value);
            var liczbaB = parseFloat(document.getElementById("liczbaB").value);

            var wynik = liczbaA + liczbaB;

            document.getElementById("wynik").textContent = wynik;
            document.getElementById("dzialanie").textContent = liczbaA + " + " + liczbaB + " = " + wynik;

            var czyParzysty = wynik % 2 === 0;
            document.getElementById("czyParzysty").textContent = czyParzysty ? "Tak" : "Nie";
        } 
    </script>
</body>
</html> 

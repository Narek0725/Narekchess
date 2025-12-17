<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Schach – Geschichte & Spiel</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Arial, sans-serif;
      background-color: #f0f0f0;
      color: #222;
      scroll-behavior: smooth; /* Sanftes Scrollen zu den Ankern */
    }

    nav {
      position: sticky;
      top: 0;
      background: #333;
      color: white;
      padding: 15px;
      text-align: center;
      z-index: 1000;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }

    nav a {
      margin: 0 15px;
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      color: #ddd;
    }

    header {
      background: linear-gradient(to right, #111, #333);
      color: white;
      text-align: center;
      padding: 80px 20px;
    }

    header h1 {
      font-size: 3rem;
      margin: 0 0 10px 0;
      text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
    }

    section {
      max-width: 800px;
      margin: 40px auto;
      padding: 40px;
      border-radius: 15px;
      background: white;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    }

    h2 {
      font-size: 2rem;
      margin-top: 0;
      color: #111;
      border-bottom: 2px solid #eee;
      padding-bottom: 10px;
    }

    p {
      line-height: 1.8;
      font-size: 1.1rem;
    }

    .image {
      width: 100%;
      border-radius: 12px;
      margin: 25px 0;
      box-shadow: 0 8px 25px rgba(0,0,0,0.2);
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.8s ease, transform 0.8s ease;
    }

    .image.show {
      opacity: 1;
      transform: translateY(0);
    }

    .image:hover {
      transform: scale(1.02);
      transition: transform 0.4s ease;
    }

    footer {
      background: #111;
      color: #888;
      text-align: center;
      padding: 30px;
      margin-top: 50px;
    }
  </style>
</head>
<body>

<nav>
  <a href="#wasist">Was ist Schach?</a>
  <a href="#geschichte">Geschichte</a>
  <a href="#heute">Heute</a>
</nav>

<header>
  <h1>Die Welt des Schachs</h1>
  <p>Entdecke die Faszination des „Königsspiels“</p>
</header>

<section id="wasist">
  <h2>Was ist Schach?</h2>
  <p>
    Schach ist ein strategisches Brettspiel für zwei Spieler, das auf einem
    8×8‑Feld gespielt wird. Ziel ist es, den gegnerischen König so anzugreifen,
    dass er nicht mehr entkommen kann – das nennt man <strong>Schachmatt</strong>.
  </p>
  <img class="image" src="https://upload.wikimedia.org/wikipedia/commons/3/30/ChessStartingPosition.jpg" alt="Schach Startaufstellung" />
</section>

<section id="geschichte">
  <h2>Ursprung & Mittelalter</h2>
  <p>
    Schach entstand vermutlich im 6. Jahrhundert in Indien unter dem Namen „Chaturanga“.
    Über Persien und die islamische Welt gelangte es im Mittelalter nach Europa, wo es
    seine heutige Form annahm.
  </p>
  <p>
    Diese Infografik zeigt die beeindruckende Entwicklung über 1500 Jahre:
  </p>
  <img class="image" src="https://zugumzug.blog/wp-content/uploads/2017/08/schach-history.png?w=700" alt="Infografik zur Geschichte" />
</section>

<section id="heute">
  <h2>Schach heute</h2>
  <p>
    Heute ist Schach populärer denn je. Dank Online-Plattformen spielen täglich Millionen 
    Menschen weltweit. Zudem haben KI-Programme wie Stockfish oder AlphaZero das 
    Verständnis des Spiels revolutioniert.
  </p>
</section>

<footer>
  © 2025 – Schach Geschichte & Spiel
</footer>

<script>
  const images = document.querySelectorAll('.image');
  
  const checkVisibility = () => {
    images.forEach(img => {
      const rect = img.getBoundingClientRect();
      if(rect.top < window.innerHeight - 50) {
        img.classList.add('show');
      }
    });
  };

  // Event Listener für Scrollen
  window.addEventListener('scroll', checkVisibility);
  // Initialer Check beim Laden
  window.addEventListener('load', checkVisibility);
</script>

</body>
</html>

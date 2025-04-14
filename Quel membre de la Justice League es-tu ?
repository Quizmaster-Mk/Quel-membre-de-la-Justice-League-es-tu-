<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quel membre de la Justice League es-tu ?</title>
  <style>
    body {
      font-family: 'Courier New', monospace;
      background-color: #101010;
      color: #f0f0f0;
      margin: 0;
      padding: 20px;
      text-align: center;
    }

    h1 {
      color: #00aeef; /* Couleur typique de la Justice League */
      text-shadow: 2px 2px 5px #ffffff;
      font-size: 40px;
      margin-bottom: 20px;
    }

    img.logo {
      max-width: 250px;
      margin-bottom: 20px;
    }

    .question {
      margin: 20px 0;
      background-color: #292929;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 174, 239, 0.7);
    }

    .options button {
      background-color: #00aeef;
      color: #fff;
      padding: 10px 20px;
      border: none;
      margin: 5px;
      font-size: 18px;
      cursor: pointer;
      border-radius: 5px;
      transition: all 0.3s ease;
    }

    .options button:hover {
      background-color: #007bb5;
      transform: scale(1.1);
    }

    .result {
      background-color: #292929;
      padding: 20px;
      border-radius: 10px;
      margin-top: 20px;
      display: none;
      box-shadow: 0 0 10px rgba(0, 174, 239, 0.7);
    }

    .score {
      font-size: 18px;
      margin-top: 10px;
      color: #ffeb3b;
    }
  </style>
</head>
<body>
  <img class="logo" src="https://zupimages.net/up/25/16/kqhz.png" alt="Logo Justice League">
  <h1>Quel membre de la Justice League es-tu ?</h1>

  <div id="quiz-container">
    <div class="question" id="question-container">
      <h2 id="question-text"></h2>
      <div class="options" id="options-container"></div>
    </div>
  </div>

  <div class="result" id="result-container">
    <h2>Tu es...</h2>
    <p id="result-text"></p>
    <p class="score">L'un des plus grands héros de l'univers DC !</p>
    <button onclick="startQuiz()">Rejouer</button>
  </div>

  <script>
    const questions = [
      { question: "Quel est ton plus grand pouvoir ?", options: ["Vitesse surhumaine", "Superforce", "Télépathie", "Maîtrise du Vol"], result: [0, 1, 2, 3] },
      { question: "Comment affrontes-tu les obstacles ?", options: ["Avec courage et détermination", "Avec ruse et intelligence", "Avec compassion", "Avec une approche tactique"], result: [0, 1, 2, 3] },
      { question: "Quel est ton but ultime ?", options: ["Protéger l'humanité", "Gérer l'équilibre de l'univers", "Mettre fin aux injustices", "Inspirer les autres à se battre"], result: [1, 0, 2, 3] },
      { question: "Si tu avais un adversaire, que ferais-tu ?", options: ["Je me battrais jusqu'à la fin", "Je chercherais à comprendre leur point de vue", "J'utiliserais ma force mentale", "Je réfléchirais à une solution stratégique"], result: [0, 1, 2, 3] },
      { question: "Dans un groupe, quel rôle préfères-tu ?", options: ["Le leader", "L'analyste", "Le protecteur", "Le stratège"], result: [0, 1, 2, 3] }
    ];

    const characters = [
      { name: "Superman", description: "Le dernier fils de Krypton, doté d'une force incroyable et de la capacité de voler." },
      { name: "Batman", description: "L'homme qui ne dort jamais, un maître du combat et de la stratégie, avec une intelligence et une détermination sans égales." },
      { name: "Wonder Woman", description: "La princesse amazone, une guerrière d'une force inouïe, dotée d'une volonté inébranlable." },
      { name: "Flash", description: "Le maître de la vitesse, toujours le premier à intervenir pour sauver la situation." },
      { name: "Green Lantern", description: "Un membre des Green Lantern Corps, un héros dont la volonté est plus forte que n'importe quelle peur." },
      { name: "Aquaman", description: "Le roi d'Atlantis, capable de communiquer avec les créatures marines et de maîtriser l'océan." },
      { name: "Martian Manhunter", description: "Un Martien doté de capacités télépathiques et de métamorphisme, un protecteur discret de la Terre." }
    ];

    let currentQuestion = 0;
    let userAnswers = [];

    function startQuiz() {
      currentQuestion = 0;
      userAnswers = [];
      document.getElementById('result-container').style.display = 'none';
      document.getElementById('quiz-container').style.display = 'block';
      showQuestion();
    }

    function showQuestion() {
      const question = questions[currentQuestion];
      document.getElementById('question-text').innerText = question.question;

      const optionsContainer = document.getElementById('options-container');
      optionsContainer.innerHTML = '';

      question.options.forEach((option, index) => {
        const button = document.createElement('button');
        button.innerText = option;
        button.onclick = () => {
          userAnswers.push(question.result[index]);
          currentQuestion++;
          if (currentQuestion < questions.length) {
            showQuestion();
          } else {
            showResult();
          }
        };
        optionsContainer.appendChild(button);
      });
    }

    function showResult() {
      const resultIndex = userAnswers.reduce((a, b) => a + b, 0) % characters.length;
      const result = characters[resultIndex];
      document.getElementById('result-text').innerText = `${result.name} - ${result.description}`;
      document.getElementById('quiz-container').style.display = 'none';
      document.getElementById('result-container').style.display = 'block';
    }

    startQuiz();
  </script>
</body>
</html>

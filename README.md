<h1 align="center">Hi 👋, I'm terbinosab</h1>



  <style>
    .container {
  text-align: center;
  margin-top: 50px;
}

.board {
  display: grid;
  grid-template-columns: repeat(3, 100px);
  grid-template-rows: repeat(3, 100px);
  gap: 5px;
  background-color: #333;
  padding: 5px;
}

.board > div {
  border: 2px solid #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2em;
  color: #fff;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.board > div:hover {
  background-color: #555;
}

.message {
  margin-top: 20px;
  font-size: 1.5em;
  color: #fff;
}

.reset-btn {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 1em;
  cursor: pointer;
  background-color: #ff5733;
  color: #fff;
  border: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.reset-btn:hover {
  background-color: #ff7f5e;
}
/* Media Query for smaller screens */
@media only screen and (max-width: 600px) {
  .board {
    grid-template-columns: repeat(3, 80px);
    grid-template-rows: repeat(3, 80px);
  }
}
  </style>

  <div class="container">
    <h1>O X Game</h1>
    <div id="board" class="board"></div>
    <div id="message" class="message">Player 1's turn (O)</div>
    <button id="resetBtn" class="reset-btn">Reset</button>
  </div>
  <script src="m.js">
    const board = document.getElementById('board');
const message = document.getElementById('message');
const resetBtn = document.getElementById('resetBtn');

let currentPlayer = 'O';
let boardState = ['', '', '', '', '', '', '', '', ''];
let gameActive = true;

const winningConditions = [
  [0, 1, 2],
  [3, 4, 5],
  [6, 7, 8],
  [0, 3, 6],
  [1, 4, 7],
  [2, 5, 8],
  [0, 4, 8],
  [2, 4, 6]
];

function handleCellClick(index) {
  if (!gameActive || boardState[index] !== '') return;

  boardState[index] = currentPlayer;
  renderBoard();
  if (checkWin()) {
    message.innerText = `${currentPlayer} wins!`;
    gameActive = false;
    return;
  }
  if (checkDraw()) {
    message.innerText = `It's a draw!`;
    gameActive = false;
    return;
  }
  currentPlayer = currentPlayer === 'O' ? 'X' : 'O';
  message.innerText = `Player ${currentPlayer}'s turn`;
}

function checkWin() {
  return winningConditions.some(condition => {
    return condition.every(index => {
      return boardState[index] === currentPlayer;
    });
  });
}

function checkDraw() {
  return boardState.every(cell => cell !== '');
}

function renderBoard() {
  board.innerHTML = '';
  boardState.forEach((cell, index) => {
    const cellElement = document.createElement('div');
    cellElement.innerText = cell;
    cellElement.classList.add('cell');
    cellElement.addEventListener('click', () => handleCellClick(index));
    board.appendChild(cellElement);
  });
}

function resetGame() {
  currentPlayer = 'O';
  boardState = ['', '', '', '', '', '', '', '', ''];
  gameActive = true;
  message.innerText = `Player ${currentPlayer}'s turn`;
  renderBoard();
}

resetBtn.addEventListener('click', resetGame);

resetGame();

  </script>

<h3 align="center">A passionate frontend developer from Ethiopia</h3>
![Placeholder](https://via.Icons.jpg.com/150)

<p align="left"> <img src="https://github.com/terbinosab" alt="terbinosab" /> </p>
<img align="right" alt="Coding" src=".jpg">
<p align="left"> <a href="https://github.com/ryo-ma/github-profile-trophy"><img src="https://github-profile-trophy.vercel.app/?username=terbinosab" alt="terbinosab" /></a> </p>


- 🌱 I’m currently learning **courses**

- 📫 How to reach me **terbinosabebebirbirsa@gmail.com**

<h3 align="left">Connect with me:</h3>
<p align="left">
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://www.blender.org/" target="_blank" rel="noreferrer"> <img src="https://download.blender.org/branding/community/blender_community_badge_white.svg" alt="blender" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> </p>


<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=terbinosab&show_icons=true&locale=en&layout=compact" alt="terbinosab" /></p>

<br> 

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=terbinosab&show_icons=true&locale=en" alt="terbinosab" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=terbinosab&" alt="terbinosab" /></p>

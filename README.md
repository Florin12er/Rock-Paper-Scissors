# Rock-Paper-Scissors

const values = ["rock", "paper", "scissors"];

function playerSelection() {
  let player = prompt("Choose: rock, paper, or scissors");
  let valueWritten = player.toLowerCase();
  return valueWritten;
}

function getComputerChoice() {
  let choice = computerChoice();
  let computerValue = choice;
  return computerValue;
}

function computerChoice() {
  return values[Math.floor(Math.random() * values.length)];
}

function playRound() {
  let userChoice = playerSelection();
  let computerChoice = getComputerChoice();

  switch (true) {
	case computerChoice === "scissors" && userChoice === "paper":
	  alert("Computer chose scissors. You lose Stefan ): !");
	  break;
	case computerChoice === "rock" && userChoice === "scissors":
	  alert("Computer chose rock. You lose Stefan ):!");
	  break;
	case computerChoice === "paper" && userChoice === "rock":
	  alert("Computer chose paper. You lose Stefan ): !");
	  break;
	case computerChoice === "scissors" && userChoice === "rock":
	  alert("Computer chose scissors. You win!");
	  break;
	case computerChoice === "rock" && userChoice === "paper":
	  alert("Computer chose rock. You win!");
	  break;
	case computerChoice === "paper" && userChoice === "scissors":
	  alert("Computer chose paper. You win!");
	  break;
	case computerChoice === userChoice:
	  alert("It's a tie!");
	  break;
	default:
	  alert("Invalid input. Please choose rock, paper, or scissors.");
  }
}
playRound();
playRound();
playRound();
playRound();
playRound();


# Number_game

let round = 1;
let userTurn;
let userMoves = 0;
let computerTurn;
let ComputerMoves = 0;
let drawRound = 0;
console.log("We are going to play \nSnake = 1\nWater = 2\n and Gun = 3.");

while (round <= 3) {
userTurn = prompt("Enter Numbers from 1 to 3: ");
userTurn = parseInt(userTurn);
computerTurn = Math.floor(Math.random() * 3) + 1;
console.log("User chose", userTurn);
console.log("Computer chose", computerTurn);

if (
(userTurn == 1 && computerTurn == 2) ||
(userTurn == 3 && computerTurn == 1) ||
(userTurn == 2 && computerTurn == 3)
) {
console.log("User Wins this Round.........");
userMoves++;
} else if (
userTurn < 1 ||
userTurn > 3 ||
computerTurn < 1 ||
computerTurn > 3
) {
console.log("Enter the Correct Prescribed Number, Try Again!!!");
break;
} else if (userTurn == computerTurn) {
console.log("Round Draw..........");
drawRound++;
} else {
console.log("Computer Wins this round.............");
ComputerMoves++;
}

round++;
}

if (round === 3) {
console.log(
user's points are: ${userMoves}, and computers's points are: ${ComputerMoves}
);
if (userMoves > ComputerMoves && userMoves > drawRound) {
console.log(User wins the game with ${userMoves});
} else if (drawRound > ComputerMoves && drawRound > userMoves) {
console.log(Game has become DRAW!!!!!);
} else if ((drawRound == ComputerMoves) == userMoves) {
console.log("NO one won the game.........");
} else {
console.log(Computer wins the game with ${ComputerMoves});
}
} else {
console.log("Number selection from the user was not correct");

}

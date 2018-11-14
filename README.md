# unit-4-game
unit-4-game
 
#Content for my game begins on line 40 and ends 74.
#Crystals images Line 41 to 58
#Game displays start number, player number wins and losses are located 59 to 64
# line 91 starts the javascript

#Listed below creates Random Number for each crystal
var crystal1 = Math.floor(Math.random() * 3) + 1;
var crystal2 = Math.floor(Math.random() * 6) + 1;
var crystal3 = Math.floor(Math.random() * 9) + 1;
var crystal4 = Math.floor(Math.random() * 12) + 1;

#Listed below creates Random Number for match 2 vatiables will generate a numver between 19-20
function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1) + min);            
            }
#RESETS GAME GENERATES NEW NUMBERS FOR CRYSTALS AND RAMDOM MATCH          
function resetGame(){
              startNumber = getRandom(min, max);
              playerNumber = 0;
              crystal1 = Math.floor(Math.random() * 3) + 1;
              crystal2 = Math.floor(Math.random() * 6) + 1;
              crystal3 = Math.floor(Math.random() * 9) + 1;
              crystal4 = Math.floor(Math.random() * 12) + 1;
              $("#crystal-1").val(crystal1);
              $("#crystal-2").val(crystal2);
              $("#crystal-3").val(crystal3);
              $("#crystal-4").val(crystal4);
              $("#start-number-display").text(startNumber);
            }

#records startCalculator() clicks a updates the diplays
function startCalculator(){
              playerNumber = 0;
              playerNumber2 = 0;
              firstNumber = 0;
            }
            
             $("#crystal-1").on("click", function(){
               playerNumber += crystal1;
             console.log("click1" ,(playerNumber));
             firstNumber = parseInt(playerNumber);
              $("#your-number-display").text(firstNumber);
             })

             $("#crystal-2").on("click", function(){
                
              playerNumber += crystal2;
             console.log("click2" ,(playerNumber));
             firstNumber = parseInt(playerNumber);
              $("#your-number-display").text(firstNumber);
             
             }) 
             $("#crystal-3").on("click", function(){
              playerNumber += crystal3;
             console.log("click3" ,(playerNumber));
             firstNumber = parseInt(playerNumber);
              $("#your-number-display").text(firstNumber);
             })

             $("#crystal-4").on("click", function(){
              playerNumber += crystal4;
              firstNumber = parseInt(playerNumber);
              $("#your-number-display").text(firstNumber);
              })
              console.log(" fn",startCalculator.firstNumber);
              console.log(" sn",startNumber);
          

            
            startCalculator();
console.log(" playerNumber end",startCalculator.playerNumber);
            /// playerNumber += $(this).val();
              
          
            
            console.log(" startNumber start",startNumber);
        
        $(".number").on("click", function() {
        
          if (firstNumber === startNumber) {
            outcome = "Yes-It's equal";
            wins++;
            game++;
            resetGame();      
            }
          else if (firstNumber === 0) {
            outcome = "No";

            }
          else  if (firstNumber > startNumber) {
            outcome = "You Went Over!"
            loss++;
            resetGame();
          ///  game= game + 1;     
            }  
        $("#your-number-wins").text(wins);
        $("#your-number-loss").text(loss);
                   
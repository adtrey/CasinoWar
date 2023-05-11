Asher Dauer & Raanan Glashofer
CasinoWar
Stage 1: User Centered Design
Who uses it?
People who want an online version of Casino War. 
Why does he use it? What is he trying to accomplish when he uses it?
He wants to
Experience the thrill/fun of gambling 
Make money
What functions does your software provide to the user that help him achieve his goal(s)?
Our software provides easy access to Casino War online instead of having to visit a Casino
The player has the ability to set a limit on his losses, ensuring the gambling does not get out of control. 
How does he use it? What steps does he go through in order to achieve his goal(s)? What are the workflows he progresses through when using it?
He uses it by first providing a balance and a betting limit (which will automatically cut off all gameplay when reached).
After this he can enter a game and dictate his bet amount each hand.
In order to be successful, he has to defeat the house advantage/odds and win hands. 
He will be able to check his career stats (balance, total hands played, and total win percentage).


Stage 2: Data Model
Player Class
Instance Variables - balance (double), totalHandsPlayed (int), playerWins (int), userID (int), name (String)

Methods:
Withdraw
Deposit
Enter Game
Leave Game
double getWinPercentage()
int getTotalHandsPlayed()

House Class
Singleton file
Instance Variables - totalHandsPlayed (int), houseWins (int), HouseBalance(double), AggregatePlayerBalance(double), players (Set), HouseOnline (Boolean),


Methods:
double getWinPercentage()
boolean checkHouseBalanceIsSufficient(double house, double players)

Deck Class
Instance variables - Array of length 52
Constructor - Fill deck  
	Sub class: Card:
		Instance Variables
int value
Enum suit

Methods: 
pickRandomCard
fillDeck()

Game Class
Instance Variables - player (Player), house (House), deck (Deck)

Methods:
void playHand(int bet)
void updateRecords()
Not necessary for now: asCard (for UI)

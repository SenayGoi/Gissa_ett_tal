# Gissa_ett_tal
Inlämningsuppgift projektarbete
Välj en siffra mellan 1 och 100
Jag skapade ett projekt där jag skapade ett program för ett gissningsprogram där folk får 10 försök att välja ett tal mellan 1 och 100. Programmet går ut på att den frågar användaren som ska mata in en siffra det kommer upp en pront som begär en användare att gissa en siffra. Programmet väljer ut en slumpmässig siffra mellan 1 och 100 varje gång programmet körs. Jag har gjort så att man har 10 försök att välja rätt siffra. Efter 10 försök så säger den att spelet är över och sedan så berättar den vilken siffra det var.
Till hjälp som man gissar så säger programmet om siffran är lägre eller högre än vad programmet har valt. 
Foreloop använde jag för att jag ville att den ska få fler chanser på sig att välja rätt siffra.
När man anropar metoden random får man som resultat ett slumpmässigt tal av typen double. Talet är större än eller lika med noll och mindre än ett.  
Mitt program hade lägsta talet 1 därför adderade jag in 1 in min kod. Därefter så multiplacerade jag talet med 100 så att i praktiken så kan det största talet endast vara 100. 
svar = (int) (1 + Math.random() * 100);

Krav
Ett av kraven är att programmet inte ska krascha om man skriver in en bokstav. 
Man ska inte kunna skriva en siffra som är större än 100(man får meddelande talet är för stort)
Man ska inte kunna välja med än 10 försök att välja en siffra.




int svar, guess = 0, x = 0;
int guess är den variabeln som vi förvarar svaren från användarna gissning
in svar är den variabeln som där vi förvarar den slumpmässiga siffran som användaren ska gissa fram.
Dessa två variablernas uppgift är att kunna jämföra med varandra för att kunna se om användrana har gissat rätt eller fel.
Guess
Vi sätter värdet noll i variabeln guess i början av spelet.
0, x = 0;
Varibalen x är hjälp räknare där vi förvarar en int, den räknar antal gissningar användaren har gjort.
boolean correct = false;
variablen correct boolean vi använder den för att kunna avgöra det typen av värde som användaren matar in i programmet.
Vi initierar den som false för att programmet inte ska gå vidare med felaktigt inmatning från användaren och krascha,
svar = (int) (1 + Math.random() * 100);
I början av programmet så låter vi programmet välja en slumpmässigt siffra mellan 1 och 100 och sparar den i variabeln.
Scanner keyboard = new Scanner(System.in);
Den startar upp en ny scanner för att kunna ta emot inputs.
Try and catch metoder använder jag för att avgöra den inmatade datatypen om det är en int eller inte. Om det är en int så ändrar vi variabeln värdet correct till true. Om det visar sig inte är en int så används catch för att fånga felmeddelandet i catch metoder samt skriver ut att spelet är avslutat .Vi sparar ner det inmatade värdet i guess och ändrar correct till true. 
if(correct 
om det inmattade värden visar sig vara correct så har variabeln correct ändras till true då fortsätter programmet.  (4 st if satser)
for (int i = 0; i < 9; i++) {
jag använder en forlop för att användaren ska kunna gissa 10 gånger.
I forloppen så har jag if satser för att hjälpa användaren med gissningar som ledtrådar. I varje if sats så finns det samma try and catch metod som tidigare som används för att avgöra om användaren har matat in en int eller inte. Om använderen inte så fortsätter spelet annars avslutades det. Break; avslutar forloppen
Jag använder if satsen för att hjälpa användaren att komma fram till vad rätt svar är som ledtrådar om talet är fort stort eller mindre eller över 100. Om man gissar rätt så avslutas spelet.
Sista if satsen är till för spelaren berättar för spelaren att man har gissat över 10 gånger och den skriver ut vad svaret var.
 x++;
Här räknar den upp plus 1 efter gissningar om det har matats in en int så räknar den plus 1 för att hålla reda på hur gissningar användaren har gjort.

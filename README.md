Download Link: https://assignmentchef.com/product/solved-cs2124-homework-6-cyclic-association-and-separate-compilation
<br>
<strong>Focus</strong>

<ul>

 <li>Cyclic Association</li>

 <li>Operator overloading</li>

 <li>Separate compilation</li>

 <li>Namespace</li>

</ul>

<strong>Problem:</strong>

We are revisiting the world of Nobles and Warriors (hoping you aren’t sick of it…), now adding one new feature: not only can warriors be fired, they can also runaway!!! Of course, when a warrior runs away, he has to inform his noble. Which means the warrior has to know who hired him and be able to communicate with him. Which means, obviously, that he will need a pointer to his noble.  Good thing we learned about forward class declarations!

You will also:

<ul>

 <li>Place all method definition outside of the their classes</li>

 <li>Use separate compilation for all methods, giving each class its own header and implementation files.

  <ul>

   <li>Yes, this item implies the first. But if you haven’t covered separate compilation yet, you can do most of the work but just handling the first bullet for now. The rest should get covered sufficiently before the due date.</li>

  </ul></li>

 <li>Place the code in the WarriorCraft namespace.</li>

</ul>

<strong>Test Code and Output</strong>

Below is a test program and its output. The only change in the test program from the one in hw04 is that cheetah runs away, rather than getting fired. (Yes, a noble should still be able to fire a warrior.) The output should also only be different in the one line of output corresoponding to cheetal running away.

#include “Noble.h”

#include “Warrior.h”

#include &lt;iostream&gt;

#include &lt;vector&gt;

#include &lt;string&gt;

using namespace std;

using namespace WarriorCraft;




int main() {

Noble art(“King Arthur”);

Noble lance(“Lancelot du Lac”);

Noble jim(“Jim”);

Noble linus(“Linus Torvalds”);

Noble billie(“Bill Gates”);




Warrior cheetah(“Tarzan”, 10);

Warrior wizard(“Merlin”, 15);

Warrior theGovernator(“Conan”, 12);

Warrior nimoy(“Spock”, 15);

Warrior lawless(“Xena”, 20);

Warrior mrGreen(“Hulk”, 8);

Warrior dylan(“Hercules”, 3);




jim.hire(nimoy);

lance.hire(theGovernator);

art.hire(wizard);

lance.hire(dylan);

linus.hire(lawless);

billie.hire(mrGreen);

art.hire(cheetah);




cout &lt;&lt; jim &lt;&lt; endl;

cout &lt;&lt; lance &lt;&lt; endl;

cout &lt;&lt; art &lt;&lt; endl;

cout &lt;&lt; linus &lt;&lt; endl;

cout &lt;&lt; billie &lt;&lt; endl;




cheetah.runaway();

cout &lt;&lt; art &lt;&lt; endl;




art.battle(lance);

jim.battle(lance);

linus.battle(billie);

billie.battle(lance);

}

Jim has an army of 1

Spock: 15

Lancelot du Lac has an army of 2

Conan: 12

Hercules: 3

King Arthur has an army of 2

Merlin: 15

Tarzan: 10

Linus Torvalds has an army of 1

Xena: 20

Bill Gates has an army of 1

Hulk: 8

Tarzan flees in terror, abandoning his lord, King Arthur

King Arthur has an army of 1

Merlin: 15

King Arthur battles Lancelot du Lac

Mutual Annihalation: King Arthur and Lancelot du Lac die at each other’s hands

Jim battles Lancelot du Lac

He’s dead, Jim

Linus Torvalds battles Bill Gates

Linus Torvalds defeats Bill Gates

Bill Gates battles Lancelot du Lac

Oh, NO!  They’re both dead!  Yuck!
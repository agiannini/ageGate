AGE GATE

The 'Age Gate' uses vanilla JavaScript, cookies and Bootstrap's modal class to prompt users for their birthdays before entering a site. 

To see the gate's functionality, open the ageGate.html, or visit https://agiannini.github.io/ageGate/ageGate.html.

To implement the gate into another site, add ageGate.js to the site's static folder and copy the contents of the body of ageGate.html into the body tag in the home page (This includes all style dependencies like fonts and bootstrap cdn). To include background and logo save files as gate_logo.jpg, and gate_background.jpg. To see the gate in another context visit http://162.243.172.246:4000/#/home . These two examples are identical, except for the gate_logo.jpg and gate_background.jpg files.

The ageGate consists of four files: ageGate.js, ageGate.html, gate_logo.jpg, gate_background.jpg. ageGate.js has a global const variable called AGE_LIMIT which sets the gate’s age limit. The user can easily change the limit by changing this variable. 

The gate calls on two jpg images called gate_background.jpg and get_logo.jpg. For the purposes of this project, I used New York Distillery’s logo and background.

The general flow of control is: the program checks to see if the isValid Cookie is set to ‘true’. If so, it displays the home page as normal. If not, it creates a modal, which prevents the user from seeing the page underneath. The modal contains a form which allows the User to enter their birthdate. The form is then validated with the validate() function (this is done with a Date object (called TODAY) and the AGE_LIMIT variable). If valid, the modal disappears and displays the page. If not, an alert is displayed and the page is reloaded.

The modal also contains a checkbox. If the user enters a valid birthday and the box is checked, an isValid cookie will be created on the user's computer. If the box is checked and the user enters an invalid birthday, the cookie will not be set. 

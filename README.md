AGE GATE

The 'Age Gate' uses vanilla JavaScript, cookies and Bootstrap's modal class to prompt users for their birthdays before entering a site. 

To see the gate's functionality, open the ageGate.html, or visit https://agiannini.github.io/ageGate/ageGate.html. For this example, I used New York Distillery’s logo and background.

To see the gate in another context visit http://162.243.172.246:4000/#/home . These two examples are identical, except for the gate_logo.jpg and gate_background.jpg files.

The ageGate consists of four files: ageGate.js, ageGate.html, gate_logo.jpg, gate_background.jpg. ageGate.js has a global const variable called AGE_LIMIT which sets the gate’s age limit. The user can easily change the limit by changing the value of this variable. 

The general flow of control is: the program checks to see if the isValid Cookie is set to ‘true’. If so, it displays the home page as normal. If not, it creates a modal, which prevents the user from seeing the page underneath. The modal contains a form which allows the User to enter their birthdate. The form is then validated with the validate() function (this is done with a Date object (called TODAY) and the AGE_LIMIT variable). If valid, the modal disappears and displays the page. If not, an alert is displayed and the page is reloaded.

The modal also contains a checkbox. If the user enters a valid birthday and the box is checked, an isValid cookie will be created on the user's computer. If the box is checked and the user enters an invalid birthday, the cookie will not be set. 

The folder contains two essential files: ageGate.js and ageGate.html. To implement the gate into another site, add ageGate.js to the site's folder and copy the contents within the body tag of ageGate.html into the body tag in the new site (the html needed is marked by comments). In addition, the folder contains two non-essential files: gate_logo.jpg and gate_background.jpg. The program assumes that they are in the same folder as the html. To include original background and logo files, save them as gate_logo.jpg, and gate_background.jpg or modify the html file names. 

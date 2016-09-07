# Trello-CardKeeper
An Alfred 3 workflow using Trello add-card function  <br />
Add card to various trello list in various trello board with **only one keyword** !<br /><br />
 ![One keyword, various actions with key holding](/TCK-demo.gif "One keyword, various actions with key holding")<br /><br />

## The idea

After testing various trello workflows for Alfred, I was surprised to find lots of bugs and misfunctions after giving my API key (probably because these workflows where not up-to-date with changes of API handling policies).

These issues kept me from using alfred as a quick way to create card in trello, whitch i do a lot for idea capturing. <br />
So i decided to make a simple trello workflow that doesn't use API key and allows you to post your card in various boards and lists easily.

## Instructions

1- Clic [This link](https://github.com/iroitosheik/Trello-CardKeeper/raw/master/Trello%20Cardkeeper%20V1.alfredworkflow) to download the workflow. Install it in Alfred opening it with alfred.

2- Clic on the *[x]* logo in the upper right corner ( named "Configure workflow and variables" )<br /><br />
    ![Clic on the Variables Menu](/Step2.png "Clic on the Variables Menu")<br /><br />

3- Change the names of *List_default , List1, List2 ...* depending on what you want to see when adding a card<br /><br />
    ![Edit List names and save](/Step3.png "Edit List names and save")<br /><br />

4- **This is the key step**, open the alfred searchbox and type <code>config tck</code> or go directly to *http://trello.com/add-card*. <br />
    Clic on the option *"create a link that adds cards to a specific board or list"* and search for the list you want to be adding trello cards to.
  
5- Once that list selected and the *"Send to trello"* shortcut created, you have to **use it to find the right "idList"**.  <br />
      Add the link in your bookmark as suggested by trello, then clic on it. <br /><br />
    ![Use the pop-up adress bar](/Step5.png "Use the pop-up adress bar")<br /><br />
      A trello page will pop up. Explore the adress bar, that should look like this : <br /> 
      https://trello.com/add-card?source=trello.com&mode=popup&url=https%3A%2F%2Ftrello.com%2Fadd-card&name=Cr%C3%A9er%20une%20carte%20Trello%20depuis%20n%27importe%20quelle%20page%20web&idList=56********************e0<br />
      Just copy the variable after *"idList="* and **paste it into alfred** variable configuration menu, under *ListXid* or *List_default_id*.<br /><br />
    ![Copy idList numbers](/Step6.png "Copy idList numbers")<br /><br />
      
6- You got it ! Your shortcut is now linked to the right board and list. **Repeat steps 4 and 5** to find other ListXid (you have 5 slots available, besides the default one)

7- To use Trello Cardkeeper, just type <code>t</code> (you can change this keyword) and our wanted card title. Press <code>ENTER</code> to send it to your *default list*. <br />
*To send it to another list, press and hold <code>⇧</code>, <code>fn</code>, <code>ctrl</code>, <code>⌘</code>, or <code>⌥</code> before validating.*

8- This will result in a page opening in your default browser, pre-filled with all your infos, just waiting to be validated ( you can even complete your card creation by adding a description ). To make this step faster, just tap <code>TAB,TAB and ENTER</code> twice.


##Limitations
**All this workflow works on the trello add-card page**. If it becomes deprecated, the workflow will not work anymore.
In that case, try the Trello official browser extension, which is pretty great !

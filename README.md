# General Assembly Project 1 - Pacman game
In this solo project, I embarked on an exciting journey to recreate a cherished childhood favourite - Pacman. Armed with JavaScript, HTML, and CSS, I immersed myself in the delightful process of bringing this classic arcade game to life.

Over the course of a week, I dedicated my efforts to crafting an engaging and functional Pacman game that would capture the essence of the original, while infusing it with a touch of creativity and innovation.

My version of Pacman boasts several compelling features that pay homage to the beloved classic:

* Two Unique Maps: I meticulously designed and incorporated two distinct maps, each offering a unique challenge and gameplay experience.
* Progression to the Next Level: Players can revel in the excitement of advancing to the next level upon successful completion of each stage.
* True to the Original: Emphasizing authenticity, I ensured that the game retained all the familiar characteristics of the classic Pacman, creating a nostalgic and enjoyable experience for players.

Try It Out!

I invite you to relive the nostalgia and embark on a thrilling Pacman adventure. Play the game here and experience the joy of chomping pellets, evading ghosts, and advancing through the levels.

Play the game here - <a href="https://thisisgurpal.github.io/pacman/">here</a>
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/159767050-f1f804e0-8cac-4005-b1fe-11dde48f4c10.JPG" width="500">

# Links
<h3>Application</h3>
Pacman: https://thisisgurpal.github.io/pacman/
<h3>Contact</h3>
Gurpal Gohler (LinkedIn): https://www.linkedin.com/in/gurpal-gohler/

# Brief
To create a game of your choice in a week using Vanilla JavaScript.

# Technologies and tools used
* JavaScript
* CSS
* HTML
* Visual Studio Code

# Walk through
<h3>Planning</h3>
When starting this project I thought about the games that I would want to build. Straight away I was drawn to Pacman as it was a game I played a lot as a kid. The next step was wireframing out the game and how I wanted the user to navigate through it, as well as what features I wanted to include. To plan the map of the game, I create a grid in JavaScript with the cell numbers and then put this into a drawing tool. Highlighting over the cells that I want the walls, points, Pacman and ghosts to be gave me a good structure to then make the grid arrays and starting points. Then I started to think where the points, levels and lives would be shown.
<h3>Home page</h3>
For the home page I made a grid that allows a ghost to move around at random and you have to click the ghost to start the game. I displayed text that has a pulse styling at the bottom of the page, this informs the user what to do. I wanted it to be fun and interactive which is why I made the home page a game in itself. When you hover over the ghost it adds a styling that will shake letting the user know that it is interactive.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161072217-b91f2eb0-8b98-4752-889e-0395958ddd43.JPG" width="500">
<h3>Choosing the map</h3>
After clicking the ghost on the home page the audio of the game starts and the user now has to choose from two different characters to play with, each character has a different game map. I wanted to have two different characters and maps to make the game a bit more fun and different for the users. I prompt the user to choose a character by adding a pulsing style to the 'CHOOSE CHARACTER' text. The two character buttons change colour and scale on hover through adding a class, this lets the user know they can be clicked. When a character is clicked a class display of none is added to this page, the game grid is set up and characters are all reset to starting positions.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161072542-3b4055d9-9710-41f6-b278-17ef37f52007.JPG" width="500">
<h3>Game countdown</h3>
This game countdown shows for 3 seconds with a number countdown, whilst this countdown is going on the Pacman and ghosts will not move and the keypad event listener is removed. After these 3 seconds a display of none is added which removes this countdown page, the ghosts move function is triggered, Pacman move function is triggered and the keypad event listener is added so you can move Pacman manually.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161073658-26efe415-b8ae-463e-bb5d-e978983f09b5.JPG" width="500">
<h3>Start eating points</h3>
Now that the game has started and you can move around using the keypad it's time to start eating all the points. Pacman is able to move by adding the Pacman class to the grid cell after determining the current direction. The points shown in the game are point classes added to the specified grid cells. So if the Pacman class and the points class are on the same grid cell, the points class is removed, the points score at the top of the page is updated and an audio is played (Pacman eats the point). 
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161074212-b79da501-4ebe-4fa6-b8bb-f181082c9560.JPG" width="500">
<h3>Losing a life</h3>
When the Pacman class and the ghosts class are in the same grid cell, we know there has been a collision. If this is the case the ghosts and Pacman are removed for a short interval, the cell in which they collided gets a class added to display a sad face, losing audio is played and the lives number at the bottom of the page is updated. After this short interval the numbers of lives left is reviewed by an if statement, if the number of lives are greater than zero the ghosts and Pacman are returned to their starting positions and the game is resumed as usual.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161074899-7f3e64e6-cd81-497a-bc13-0ba5b7f72992.JPG" width="500">
<h3>Eating a special point</h3>
I've mentioned eating points and special points are eaten the same way however something different happens in this scenario other than getting more points. Each ghost has an isScared variable that is set to false and when set to true these ghosts change their class and hence their colour changes to blue. When the Pacman class and special points class are in the same grid cell the isScared variable for all ghosts are changed to true for an interval of 10 seconds, after this period they are set back to false.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161075386-ced28917-be42-474c-a0dc-160420596b3b.JPG" width="500">
<h3>Eating a scared ghost</h3>
In this 10 second period when the ghosts are scared, if the Pacman class and scared ghost class are in the same grid cell we know there has been a collision. This collision is different as the ghost is scared. What happens now is that the grid cell the collision occurred in gets given a class to show an image with the value 100 (as you will get 100 points for eating a scared ghost) and the game stops for a second before resuming. The isScared variable of that scared ghost that has been eaten will get set back to false so it's a normal ghost again, it will also get reset to its starting point.
<h3></h3>
<table>
  <tr>
    <td valign="top"><img src="https://user-images.githubusercontent.com/97416784/161077187-8d6099d9-226d-4979-b9e5-4869cb7a4bd8.JPG" width="500"></td>
    <td valign="top"><img src="https://user-images.githubusercontent.com/97416784/161077451-4523512f-e277-47a3-a748-9fc618866574.JPG" width="500"></td>
  </tr>
</table>
<h3>Level up</h3>
Whilst Pacman is moving around the game eating points, there is a counter in background counting how many points are left in the game. Once there are no points left a page is shown letting you know the new level by removing the display of none. After a few seconds this page is removed by making the display equal to none again through the use of setTimeout. Further after this timeout, the points, Pacman and ghosts are reset and the level value at the top of the page is updated. To make the game progressively more difficult on every new level the ghosts and Pacman have their speed speed increases and a new ghost is added by pushing a random ghost into the ghosts array.
<h3></h3>
<table>
  <tr>
    <td valign="top"><img src="https://user-images.githubusercontent.com/97416784/161078526-60036586-4ec9-477d-b3fe-f836f7ea6f82.JPG" width="500"></td>
    <td valign="top"><img src="https://user-images.githubusercontent.com/97416784/161078582-b0720494-8a73-417e-bac5-376f62d9d6d9.JPG" width="500"></td>
  </tr>
</table>
<h3>Game over</h3>
When you lose a life the number of lives the user has left is assessed by an if statement. If the number of lives left is zero the game is stopped, the characters are removed and the game over page is shown using the display styling. This page is then removed after a few seconds using a setTimeout where the game will navigate to the home page using a returnToStart function. This function stops the ghost and Pacman from moving and removes the styling display of none to the home page (making it visible).
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/161079160-f32338be-e0ed-4e6c-8da1-1fc3fa442f32.JPG" width="500">

# Code examples
<h3>Adding, removing and moving Pacman</h3>
Adding and removing Pacman is done by specifying the new position then adding and removing classes to that new grid cell position.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/159753712-29da9c45-307d-4ca8-a046-687280485d08.JPG" width="700">
<img src="https://user-images.githubusercontent.com/97416784/159755095-1f5e4f3b-4333-4fe7-8128-6b8eacc47b46.JPG" width="350">
For the Pacman to move the current position and the direction need to be taken into consideration. This if statement moves Pacman for any direction chosen by the user using the arrow keys if there is not a wall already there. If the user pressed a key that is not up, down, left or right a console log is run letting you know it's an invalid key.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/159757240-e50b04ac-8da1-46d9-ad51-b2975c94c514.JPG" width="700">
To use the arrow keys to move Pacman I had to know which key is being pressed by knowing the key codes. Depending on that key it will then run the if statement in the code above using a setInterval which includes Pacman's speed.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/159758942-dbc4dbea-4a76-46c7-8a70-754667567f3d.JPG" width="700">
Adding this event listener is needed for the handleKeyDown function to be triggered when the keypad is pressed.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/159759022-32c6c45a-5885-4502-b0a9-5e7a224d03d2.JPG" width="700">
<h3>Adding Ghosts</h3>
I made a class that will enable me to add ghost's by specifying their class name, starting index and speed. In this class I have also included other variables like isScared which when set to true when Pacman eats a special point, when this happens the ghost will turn blue and can be eaten by Pacman for a period of 10 seconds.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/160430571-bc0eae65-e4c2-448a-bb8c-ef4b74ad67c0.JPG" width="700">
This is an array that I will use to interact with each ghost. If references the Ghost class to create new ghosts. If I need to add a new ghost to this array which I do for each new level, all I need to do is use the push method on this array.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/160430768-08dae014-594f-4740-9c3d-5426a6450935.JPG" width="350">
<h3>Creating the game grid</h3>
To make the grid for the game I specified the cells that don't need points, cells that need special points and the cells that need the walls. These arrays can now be used to make the grid.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/162480168-f49ce5c6-6e7b-43a2-8554-07a4e0a82cb2.JPG" width="700">
This is the function that actually makes the grid by adding classes to the specified cells in the array above. It also adds the starting values of the level, points and lives. In this function I further add Pacman and the ghosts to their starting positions.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/162480102-cdaf5f0f-a299-40be-b598-5cf0e1709702.JPG" width="700">
<h3>Starting the game</h3>
When you choose your character after the home page these functions are triggered which start preparing the starting of the game. Initially the grid is cleared, the current pages get removed, the grid is created using Pacmans starting positions, all the characters are reset, the countdown to the game is triggered, and then Pacman and the ghosts can move after a setTimeout function. This all ensures that the game is reset to its first initial level.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/162480659-a3b70d5c-353f-40cf-80ce-861865626a21.JPG" width="700">
<h3>Menu</h3>
The menu button on the game page has specific functions that get triggered depending on the buttons you click. Initially when you click the menu button the ghosts and Pacman get their intervals cleared which stops them from moving, and the keypad event listener is removed. However once you resume the game these then get set back to normal so you can play the game again.
<h3></h3>
<img src="https://user-images.githubusercontent.com/97416784/162480712-55953cf3-70a2-4cc8-98e2-265cb1520602.JPG" width="700">    

# Key Achievements and Takeaways
## Streamlined Code: Addressing Repetition
One of the notable challenges encountered during this project was dealing with repetitive code segments across different sections. To tackle this issue, I opted for a more organized approach. By creating smaller functions that performed specific tasks and reusing them throughout the codebase, I achieved not only cleaner code but also improved readability for other team members.

## Introducing the Ghosts Class: A Challenging Triumph
Another significant hurdle arose when implementing the Ghosts class to incorporate ghosts into the game. After careful consideration and reviewing my notes, I concluded that using a class would be the most effective approach. However, it posed a challenge, particularly when integrating additional elements such as the ghost's scared state (isScared). Yet, once the class structure was established, adding ghosts, adjusting their speeds, and modifying their starting positions became considerably more manageable.

## Elevating User Experience: Diverse Components and Pages
A notable accomplishment was the successful integration of different pages into the game, allowing smooth navigation. The home page, in particular, proved to be an engaging entry point to the game. Furthermore, incorporating various components during gameplay significantly enhanced the user experience. Elements like animated reactions, such as the box shaking upon beating high scores or displaying a sad face upon colliding with a ghost, added a delightful touch to the overall gameplay.

## Key Learning: Interaction of HTML, CSS, and JavaScript
Throughout this project, my primary focus was to gain proficiency in the structure of HTML, refine CSS styling, and utilize JavaScript to create functional interactions. Notably, mastering JavaScript to handle keyboard inputs and dynamically amend HTML content proved to be a valuable takeaway. Initially, I wasn't fully aware of the potential of manipulating HTML through JavaScript and creating reusable functions to improve code efficiency. This newfound knowledge empowered me to write more efficient and legible code, minimizing redundancy and promoting a modular approach.

## Future Plans: Implementing AI for Ghosts
As I reflect on this project, I feel content with its achievements, especially considering it was my first venture into this domain. However, looking ahead, an exciting future feature I envision is implementing Artificial Intelligence (AI) for the ghosts. This would introduce a new layer of challenge and engagement to the game by enabling the ghosts to intelligently follow Pacman. While I did not have the opportunity to include this feature within the current timeline, it remains a compelling goal for future iterations.
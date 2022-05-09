# Dice Game

**Practical exercise of a dinamic website**
**By: Sofía Idárraga**


Multiplayer dice game.
Demo project with a responsibilities separation using the concepts of:
- Tamplate (View)
- Logic (Controller)
- Data (Model)

### Using the code

Once the complete code is downloaded, you need to install the dependencies. (Make sure you 
are in the project ubication)

```
npm install
```
To start the project:

```
SET DEBUG=dicegame:* & npm run devstart
```

If everything is ok you should read "_MongoDB connected_" in terminal

In your web browser:

```
http://localhost:3000/
```

Now, you should on game's homepage.

## Playing

### 1. Game creation request, with its respective form:

To start the game click on **create game**

You're gonna be send to a new page 

```
> GET http://localhost:3000/createGame
```

Here you have to enter the gamers' names, and click on **send**

This open the route

```
> POST http://localhost:3000/createGame
```

You'll see here the JSON solicited at task

Now, click on **start game**

### 2. Query to check the game and its status (players list and game status at momment)

A new Menu will be open at route 
```
> GET http://localhost:3000/startGame
```

Click on **Consult Game** to open the route 
```
> GET: http://localhost:8080/game/fffff-ggg-jjjjj
```

with the solicited JSON at task, wich shows the players and the game status


### 3. Query to determine the winner (a view with the winner)

Back to Menu (it should be at an opened tab)

Click on **Consult Winner** to open the route

```
> GET: http://localhost:8080/game/fffff-ggg-jjjjj/winner
```
with the solicited JSON at task, wich shows the winner view

### 4. Request to start the game with the bet for each player (action that allows starting the game)

Back to Menu again

Click on **INFO** to open the route

```
> POST: http://localhost:3000/startGame
```
with the solicited JSON at task, wich shows each player and its bet

### Resume

Back to Menu

Click on **Resume**

A new page will be open wich shows the resume of the game: each player's bet and
the winner.

If two people got the same bet, the game will select only one.

Click on **END** to finish the game, this action will delete all the information from
MongoDB, so you can start a new game.

## Routes

Try this routes in an API platform to show the task solution.

```
> home -> localhost:3000/

"GET"
> create-game -> localhost:3000/createGame
> game-status -> localhost:3000/game/fffff-ggg-jjjjj
> game-winner -> localhost:3000/game/fffff-ggg-jjjjjwinner
> start-game -> localhost:3000/startGame

"POST"
> create-game -> localhost:3000/createGame
> start-game -> localhost:3000/startGame
```

---
⌨️by [Sofía Idárraga](https://github.com/sofia-idarraga) ?

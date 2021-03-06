# Faceit JS API
![GitHub package.json version](https://img.shields.io/github/package-json/v/Senteris/faceit-js-api) ![NPM](https://img.shields.io/npm/l/faceit-js-api) ![npm](https://img.shields.io/npm/dt/faceit-js-api)  
A small JS API for Faceit 

(If you read it on npmjs.com - Read this file on github! Npmjs.com sometimes does not see difference between face**I**t and face**i**t)
## Install
`npm install faceit-js-api`
## Documentation
### Setup
```
const Faceit = require("faceit-js-api");
const faceit = new Faceit("API KEY");
```
To test performance:
```
faceit.getPlayerInfo("Player name").then(function (player) {
    console.log(player);
});
```
### Classes
#### Faceit
Main class for performing requests
###### Methods  
| Method        | Params           | Return |
|---------------|------------------|--------|
| getPlayerInfo | nickname: string | Player |
#### Player
###### Vars
| Var           | Type   | Description                 |
|---------------|--------|-----------------------------|
| faceit        | Faceit | Link to main class          |
| nickname      | string |                             |
| id            | string |                             |
| avatar        | string | Url to avatar               |
| steamID       | string |                             |
| steamNickname | string |                             |
| faceitUrl     | string | Url to faceit profile       |
| raw           | object | All data getted from feceit |
| games         | Games  | Class with games            |
#### Games
###### Vars
| Var    | Type   | Description                                   |
|--------|--------|-----------------------------------------------|
| player | Player |                                               |
| csgo   | CSGO   | Undefined if player has not ever play CS:GO   |
| dota2  | Dota2  | Undefined if player has not ever play Dota 2  |
| wot_RU | WOT_RU | Undefined if player has not ever play WOT(ru) |
#### CSGO
###### Vars
| Var             | Type   |
|-----------------|--------|
| games           | Games  |
| gameProfileID   | string |
| gamePlayerID    | string |
| region          | string |
| skillLevelLabel | string |
| skillLevel      | int    |
| faceitElo       | int    |
| gamePlayerName  | string |
###### Methods  
| Method        | Params           | Return    |
|---------------|------------------|-----------|
| getStats      |                  | CSGOStats |
#### CSGOStats
###### Vars
| Var              | Type     |
|------------------|----------|
| csgo             | CSGO     |
| raw              | Object   |
| winRate          | string   |
| currentWinStreak | string   |
| longestWinStreak | string   |
| wins             | string   |
| recentResults    | string[] |
| averageHeadshots | string   |
| matches          | string   |
| totalHeadshots   | string   |
| kdRatio          | string   |
| averageKDRatio   | string   |
#### Dota2
###### Vars
| Var             | Type     |
|-----------------|----------|
| games           | Games    |
| gameProfileID   | string   |
| region          | string   |
| regions         | Object[] |
| skillLevelLabel | string   |
| gamePlayerID    | string   |
| skillLevel      | int      |
| faceitElo       | int      |
| gamePlayerName  | string   |
###### Methods  
| Method        | Params           | Return     |
|---------------|------------------|------------|
| getStats      |                  | Dota2Stats |
#### Dota2Stats
###### Vars
| Var              | Type     |
|------------------|----------|
| dota2            | Dota2    |
| raw              | Object   |
| currentWinStreak | string   |
| goldMinute       | string   |
| averageKDRatio   | string   |
| winRate          | string   |
| matches          | string   |
| averageGoldMinute| string   |
| result           | string   |
| recentResults    | string[] |
| kdRatio          | string   |
| longestWinStreak | string   |
#### WOT_RU
###### Vars
| Var             | Type     |
|-----------------|----------|
| games           | Games    |
| gameProfileID   | string   |
| region          | string   |
| regions         | Object[] |
| skillLevelLabel | string   |
| gamePlayerID    | string   |
| skillLevel      | int      |
| faceitElo       | int      |
| gamePlayerName  | string   |
###### Methods  
| Method        | Params           | Return      |
|---------------|------------------|-------------|
| getStats      |                  | WOT_RUStats |
#### WOT_RUStats
###### Vars
| Var                   | Type     |
|-----------------------|----------|
| wot_RU                | WOT_RU   |
| raw                   | Object   |
| averageDamageReceived | string   |
| totalDamageReceived   | string   |
| totalHitRatio         | string   |
| win                   | string   |
| totalSurvived         | string   |
| totalDamageDealt      | string   |
| averageSurvived       | string   |
| currentWinningStreak  | string   |
| averageHitRatio       | string   |
| recentResults         | string[] |
| longestWinStreak      | string   |
| totalDamageRatio      | string   |
| averageKills          | string   |
| averageDamageRatio    | string   |
| averageDamageDealt    | string   |
| winRate               | string   |
| matches               | string   |
| totalKills            | string   |

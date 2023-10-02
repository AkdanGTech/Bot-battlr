# BOT-BATTLR COLLECTIONS
Welcome to Bot Battlr, the one and only spot in the known universe where you can custom build your own Bot Army! This is our app:

# Instructions
For this project, you’ll be building out a React application that displays a list of available bots, among other features. Try your best to find the right places to insert code into the established code base.

Part of what this code challenge is testing is your ability to follow given instructions. While you will definitely have a significant amount of freedom in how you implement the features, be sure to carefully read the directions for setting up the application.

# Setup
After unbundling the project:

Run npm install in your terminal.
Run npm run server. This will run your backend on port 3000.
In a new terminal, run npm start. This will run your React app on port 3000.
Make sure to open http://localhost:3000/bots in the browser to verify that your backend is working before you proceed!

The base URL for your backend is: http://localhost:3000

What You Already Have
BotPage is the highest component below App, and serves as the main container for all of the pieces of the page.

BotCollection and YourBotArmy are container components, which are children of BotPage. BotCollection is where all the bots will be displayed, while YourBotArmy (the green portion on the top of the screen) will only display the bots that have been selected by the user.

BotCard and BotSpecs are presentational components that have been provided for you that will render out information about an individual bot formatted for a list view and for a full view, respectively. They are pre-styled, and it is your responsibility to get the data into them.

All of the code to style the page has been written for you, meaning that you should be adding to the code rather than editing it; however, if your finished product has some styling issues, don't worry too much about it.

# Core Deliverables
As a user, I should be able to:

See profiles of all bots rendered in BotCollection.
Add an individual bot to my army by clicking on it. The selected bot should render in the YourBotArmy component. The bot can be enlisted only once. The bot does not disappear from the BotCollection.
Release a bot from my army by clicking on it. The bot disappears from the YourBotArmy component.
Discharge a bot from their service forever, by clicking the red button marked "x", which would delete the bot both from the backend and from the YourBotArmy on the frontend.
Endpoints for Core Deliverables
GET /bots
Example Response:

{
  "bots": [
  
    {
      "id": 189,
      "name": "yXB-04",
      "health": 48,
      "damage": 26,
      "armor": 100,
      "bot_class": "Defender",
      "catchphrase": "111110111100011000000000111011101",
      "avatar_url": "https://robohash.org/quiomniset.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.397Z",
      "updated_at": "2018-10-02T19:55:12.397Z"
    },
    {
      "id": 190,
      "name": "c-38",
      "health": 93,
      "damage": 35,
      "armor": 44,
      "bot_class": "Medic",
      "catchphrase": "01000110010101110000101101100110000110000110011000",
      "avatar_url": "https://robohash.org/nobissimiliquequae.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.407Z",
      "updated_at": "2018-10-02T19:55:12.407Z"
    },
    {
      "id": 191,
      "name": "h-74",
      "health": 53,
      "damage": 23,
      "armor": 85,
      "bot_class": "Medic",
      "catchphrase": "11001111001000101000111000110100",
      "avatar_url": "https://robohash.org/cumomnisautem.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.417Z",
      "updated_at": "2018-10-02T19:55:12.417Z"
    },
    {
      "id": 192,
      "name": "Dls-86",
      "health": 49,
      "damage": 86,
      "armor": 29,
      "bot_class": "Assault",
      "catchphrase": "110100100001001011011010011100000010111100100",
      "avatar_url": "https://robohash.org/nullaconsequatursuscipit.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.432Z",
      "updated_at": "2018-10-02T19:55:12.432Z"
    },
    {
      "id": 193,
      "name": "M-28",
      "health": 40,
      "damage": 93,
      "armor": 21,
      "bot_class": "Assault",
      "catchphrase": "00000101111111110101111000010101",
      "avatar_url": "https://robohash.org/eumdoloredoloribus.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.447Z",
      "updated_at": "2018-10-02T19:55:12.447Z"
    },
    {
      "id": 194,
      "name": "rw-63",
      "health": 60,
      "damage": 98,
      "armor": 26,
      "bot_class": "Assault",
      "catchphrase": "11101101111011101001100000011100101110",
      "avatar_url": "https://robohash.org/molestiaenihilautem.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.463Z",
      "updated_at": "2018-10-02T19:55:12.463Z"
    },
    {
      "id": 195,
      "name": "^-52",
      "health": 81,
      "damage": 32,
      "armor": 48,
      "bot_class": "Medic",
      "catchphrase": "0111111001000010010100010110010",
      "avatar_url": "https://robohash.org/aliasquoest.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.475Z",
      "updated_at": "2018-10-02T19:55:12.475Z"
    },
    {
      "id": 196,
      "name": "obm-92",
      "health": 93,
      "damage": 23,
      "armor": 67,
      "bot_class": "Support",
      "catchphrase": "011011110001101100011000100111010100011000010",
      "avatar_url": "https://robohash.org/nulladoloratque.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.487Z",
      "updated_at": "2018-10-02T19:55:12.487Z"
    },
    {
      "id": 197,
      "name": "LvH-26",
      "health": 84,
      "damage": 26,
      "armor": 55,
      "bot_class": "Support",
      "catchphrase": "11111100001011110000010011111100111100",
      "avatar_url": "https://robohash.org/commodiidasperiores.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.503Z",
      "updated_at": "2018-10-02T19:55:12.503Z"
    },
    {
      "id": 198,
      "name": "wr-00",
      "health": 67,
      "damage": 84,
      "armor": 32,
      "bot_class": "Assault",
      "catchphrase": "111110001100001011101010110011111001000001",
      "avatar_url": "https://robohash.org/dictasolutanatus.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.512Z",
      "updated_at": "2018-10-02T19:55:12.512Z"
    },
    {
      "id": 199,
      "name": "z-06",
      "health": 41,
      "damage": 27,
      "armor": 81,
      "bot_class": "Defender",
      "catchphrase": "0101101100101100001100110000101001111010111",
      "avatar_url": "https://robohash.org/sedhicquo.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.525Z",
      "updated_at": "2018-10-02T19:55:12.525Z"
    },
    {
      "id": 200,
      "name": "fb-83",
      "health": 88,
      "damage": 38,
      "armor": 68,
      "bot_class": "Captain",
      "catchphrase": "0111100000101111011000110101110111110000",
      "avatar_url": "https://robohash.org/teneturquaereiciendis.png?size=300x300&set=set1",
      "created_at": "2018-10-02T19:55:12.537Z",
      "updated_at": "2018-10-02T19:55:12.537Z"
    }
  ]
}

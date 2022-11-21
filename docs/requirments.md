# Requirements

## User Requirements

| ID                  | Description                                                                                                                                                                     | Priority |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| UR\_COOKS\_MOVE     | Cooks must have the ability to move.                                                                                                                                            | High     |
| UR\_COOKS\_SWITCH   | Must have the ability to switch between cooks.                                                                                                                                  | High     |
| UR\_COOKS\_INTERACT | Must have the ability to chop vegetables, flip items on the stove, grab and place items.                                                                                        | High     |
| UR\_CUSTOMERS       | Customers must arrive and have a timer which will go down slowly, it dish is not severed in time then demand score is decremented                                               | High     |
| UR\_GAMEMODES       | A scenario game mode where configurable number customers arrive and they have to be served in their time limit, must have some remaining reputation points to complete.         | High     |
| UR\_STATIONS        | Must have areas where cooks are able to chop raw vegetables, cook and flip patties, bake raw ingredients, serving, picking up ingredients and a counter for customers to wait.  | High     |
| UR\_RECIPES         | This recipes for salad, burger, pizza and jacket potatoes                                                                                                                       | High     |
| UR\_SHOP            | A menu where after the game is over cooks can invest money into buying other stations and unlocking recipes. Also they will be able to call other cooking staff back from leave | Low      |


## Functional Requirements

* Cooldown after switching cooks?
* How do cooks get money?

| ID                      | Description                                                                                                                                                             | User Requirements    |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| FR\_COOKS\_MOVEMENT     | The cooks will move up, down, left, right with given the input using a keyboard                                                                                         | UR\_COOKS\_MOVE      |
| FR\_COOKS\_SWITCH       | The user will be able to switch cooks by pressing a key                                                                                                                 | UR\_COOKS\_SWITCH    |
| FR\_COOKS\_FLIP         | Must have the ability to flip items on the stove. This must be done before patty burns.                                                                                 | UR\_COOKS\_INTERACT  |
| FR\_COOKS\_GRAB         | Cooks must be able to grab items.                                                                                                                                       | UR\_COOKS\_INTERACT  |
| FR\_COOKS\_PLACE        | Cooks must be able to place items down after picking them up.                                                                                                           | UR\_COOKS\_INTERACT  |
| FR\_CUSTOMER\_ARRIVE    | Customers arrive at random time intervals and request a recipe with a dialog box that includes the required ingredients.                                                | UR\_CUSTOMER\_ARRIVE |
| FR\_GAMEMODE\_1         | A scenario game mode where configurable number customers arrive and they have to be served in their time limit, must have some remaining reputation points to complete. | UR\_GAMEMODES        |
| FR\_GAMEMODE\_2         | A “endless” game mode where customers will arrive until all reputation points are lost. The number of customers served before all points are lost is the score.         | UR\_GAMEMODES        |
| FR\_COOKING\_STATION\_1 | Must have an area where cooks are able to chop raw vegetables. If vegetables are not cut well enough must be discarded                                                  | UR\_STATIONS         |
| FR\_COOKING\_STATION\_2 | Must have an area where cooks are able to cook and flip patties, this needs to be completed in a time limit otherwise patties will burn and they have to be discarded.  | UR\_STATIONS         |
| FR\_COOKING\_STATION\_3 | This is the baking section where cooks are able to bake raw ingredients                                                                                                 | UR\_STATIONS         |
| FR\_SERVING\_STATION    | This is an area where cooks can place the made recipes and customers can receive their order                                                                            | UR\_STATIONS         |
| FR\_INGRIDENT\_STATION  | This is an area where cooks can can pick up raw ingredients to prepare, these will automatically regenerated and cooks can pick up multiple                             | UR\_STATIONS         |
| FR\_COUNTER             | This is an area where the customers will wait for their order.                                                                                                          | UR\_STATIONS         |
| FR\_RECIPE\_1           | This recipe is the salad and contains: chopped lettuce, chopped tomatoes and chopped onions. These must be stacked on a plate.                                          | UR\_RECIPES          |
| FR\_RECIPE\_2           | This recipe is the burger and contains: fried patty (must be formed first), a toasted bun. These must be stacked on a plate.                                            | UR\_RECIPES          |
| FR\_RECIPE\_3           | This recipe is a pizza and contains: a base, a sauce, a topping all stacked and then cooked.                                                                            | UR\_RECIPES          |
| FR\_RECIPE\_4           | This recipe is a jacket potato containing: a cooked potato and a topping stacked on a plate.                                                                            | UR\_RECIPES          |
| FR\_SCORE               | This is a variable that is initially 3 and when a demand is not met it will decrement                                                                                   | UR\_CUSTOMER         |
| FR\_CUSTOMER\_ARRIVE    | Customers will arrive at a given random time interval. They will initial arrive on their own then in groups                                                             | UR\_CUSTOMER         |
| FR\_CUSTOMER\_DEMAND    | When a customer arrives they will request an item and give a time limit.                                                                                                | UR\_CUSTOMER         |
| FR\_MONEY               | This is a score when a customer is served within the time frame the player will be rewarded some money.                                                                 | UR\_SHOP             |
| FR\_SHOP\_MENU          | This is menu where the player can spend coins on more stations and cooks                                                                                                | UR\_SHOP             |


## Non-Functional Requirements

* How long should each game last?
* What difficulty level should be?
* What is the time limit for waiting customers?
* How long should items take to cook?
* Should recipes be displayed?
* What sort of movement? speed, direction?
* Can you stack raw items?

| ID                     | Description                                                                            | User Requirements   | Fit Criteria                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------- | ------------------- | ----------------------------------------------------------------------------------------------- |
| NFR\_MOVE\_ACCESSIBLE  | The game should have basic controls that are easy to learn.                            | UR\_MOVE            | All ages and abilities should be able to move                                                   |
| NFR\_CONTROL\_RESPONDS | The response time should be real-time and instant.                                     | UR\_MOVE            | The controls should have instance >0.01 seconds                                                 |
| NFR\_STACKING\_ITEMS   | The items should be able to be stacked in any order.                                   | UR\_RECIPES         | Prepped ingredients need to be present                                                          |
| NFR\_COOKING\_TIME     | Chopping and cooking should be completed in reasonable time.                           | UR\_STATIONS        | Takes >5 seconds                                                                                |
| NFR\_CUSTOMER\_DEMAND  | Must allow for enough time to complete recipe                                          | UR\_CUSTOMER        | Demand >60 seconds                                                                              |
| NFR\_SWITCH            | Switching must be fast and responsive                                                  | UR\_SWITCH          | Only slight cooldown time 1 second                                                              |
| NFR\_WAITING           | The game must provide an easy way of seeing recipe requests and time left to complete. | UR\_CUSTOMER        | Have a bar telling to customers have ordered and how long the cooks have to complete the order. |
| NFR\_ TUTORIAL         | Game should provide a training environment where user can learn to play the game       | UR\_MOVE            | Have a tutorial mode allowing new users to learn the game.                                      |
| NFR\_AUDIO\_CUES       | Game should have audio cues to action that a relevant and recognisable                 | UR\_COOKS\_INTERACT | Audio will help the game be engaging and confirm action has been performed                      |
| NFR\_ENGAMENT          | Games should be fun and make it easy to play.                                          | UR\_GAMEMODES       | Game should be engaging for all users                                                           |

# Constraint Requirements

* Stakeholder: The University of York Communications Office
* Customers: Lectures
* All software use must be open source and free
* Must be made in Java
* What kind of systems should it run on?

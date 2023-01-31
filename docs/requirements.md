# Requirements

[Requirements Specification Document](pdf/Req1.pdf)



# User Requirements
| ID               	| Description                                                                                                                                                                           	| Priority 	|
|------------------	|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|----------	|
| UR_COOKS         	| Cooks must have the ability to move.                                                                                                                                                  	| High     	|
| UR_CUSTOMERS     	| Customers must arrive and have a timer which will go down slowly. If a dish is not served in time then the demand score is decremented.                                               	| High     	|
| UR_GAMEMODES     	| This entails two game modes: a scenario gamemode with a set amount of customers to serve in a limited time, and an endless gamemode where you play until you run out of points.       	| High     	|
| UR_STATIONS      	| These are areas where cooks can chop raw vegetables, cook and flip patties, bake raw ingredients, serve, pick up ingredients and a counter for customers to wait.                     	| High     	|
| UR_RECIPES       	| This includes recipes for salad, burger, pizza and jacket potatoes.                                                                                                                   	| High     	|
| UR_SHOP          	| A menu where cooks can invest money into buying new stations and recipes after the game is over. They will also be able to call other cooking staff back from leave.                  	| Low      	|
| UR_IDLE          	| An idle mode where the game will play itself if nobody is playing.                                                                                                                    	| High     	|
| UR_ACCESSIBILITY 	| The game will be played by a lot of different people on an open-day, some may be far away from the screen and the environment will be noisy; as such, it should be accessible to all. 	| High     	|

# Functional Requirements
| ID                   	| Description                                                                                                                                                                                   	| User Requirements 	|
|----------------------	|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|-------------------	|
| FR_COOKS_MOVEMENT    	| The cooks will move up, down, left and right with the given input using a keyboard.                                                                                                           	| UR_COOKS          	|
| FR_COOKS_SWITCH      	| The user will be able to switch cooks by pressing a key.                                                                                                                                      	| UR_COOKS          	|
| FR_COOKS_FLIP        	| Must have the ability to flip items on the stove. This must be done before patty burns.                                                                                                       	| UR_COOKS          	|
| FR_COOKS_CHOP        	| Must have the ability to chop items at the relevant station..                                                                                                                                 	| UR_COOKS          	|
| FR_COOKS_GRAB        	| Cooks must be able to grab items and can hold up to 2 items, one in each hand.                                                                                                                	| UR_COOKS          	|
| FR_COOKS_PLACE       	| Cooks must be able to place items down in the same order they picked them up in.                                                                                                              	| UR_COOKS          	|
| FR_CUSTOMER_ARRIVE   	| Customers arrive at random time intervals and request a recipe with a dialog box that includes the required ingredients. In the scenario they will arrive on their own, then later in groups. 	| UR_CUSTOMERS      	|
| FR_GAMEMODE_1        	| A scenario game mode where a configurable number of customers arrive who must be served in the time limit. Requires reputation points to complete.                                            	| UR_GAMEMODES      	|
| FR_GAMEMODE_2        	| An “endless” game mode where customers will arrive until all reputation points are lost. The number of customers served before all points are lost serves as the score.                       	| UR_GAMEMODES      	|
| FR_COOKING_STATION_1 	| Must have an area where cooks are able to chop raw vegetables. Vegetables must be cut properly.                                                                                               	| UR_STATIONS       	|
| FR_COOKING_STATION_2 	| Must have an area where cooks are able to cook and flip patties. This must be done within a time limit otherwise the patties will burn and end up discarded.                                  	| UR_STATIONS       	|
| FR_COOKING_STATION_3 	| This is the baking section where cooks are able to bake raw ingredients.                                                                                                                      	| UR_STATIONS       	|
| FR_SERVING_STATION   	| This is an area where cooks can place the complete dishes and customers can receive their order.                                                                                              	| UR_STATIONS       	|
| FR_INGRIDENT_STATION 	| This is an area where cooks can pick up raw ingredients to prepare. These will automatically be replenished and cooks can pick up multiple at once.                                           	| UR_STATIONS       	|
| FR_COUNTER           	| This is an area where the customers will wait for their order.                                                                                                                                	| UR_STATIONS       	|
| FR_RECIPE_1          	| This recipe for salads contains chopped lettuce, chopped tomatoes and chopped onions. They must be stacked on a plate.                                                                        	| UR_RECIPES        	|
| FR_RECIPE_2          	| This recipe for burgers contains a fried patty (must be formed first) and a toasted bun. These must be stacked on a plate.                                                                    	| UR_RECIPES        	|
| FR_RECIPE_3          	| This recipe for pizzas contains a base, a sauce and a topping, all stacked and then cooked.                                                                                                   	| UR_RECIPES        	|
| FR_RECIPE_4          	| This recipe for jacket potatoes contains a cooked potato and a topping, both stacked on a plate.                                                                                              	| UR_RECIPES        	|
| FR_RECIPE_DISPLAY    	| Recipes will be displayed as pictures of the ingredients to make up the order.                                                                                                                	| UR_RECIPES        	|
| FR_SCORE             	| A variable that initially starts at 3. When a customer’s demand is not met, it will decrease.                                                                                                 	| UR_CUSTOMERS      	|
| FR_CUSTOMER_WAIT     	| Customers will wait at a counter while their order is being prepared. If they wait too long then there will be a point penalty.                                                               	| UR_CUSTOMERS      	|
| FR_CUSTOMER_DEMAND   	| When a customer arrives they will request an item and give a time limit. If this isn’t completed within the time limit then there will be a point penalty.                                    	| UR_CUSTOMER       	|
| FR_MONEY             	| One of the score metrics. If a customer is served within the time frame, the player will be rewarded with some money.                                                                         	| UR_SHOP           	|
| FR_SHOP_MENU         	| A menu where the player can spend money on more stations and cooks.                                                                                                                           	| UR_SHOP           	|
| FR_IDLE_MODE         	| An option in the game menu where the user can choose to not play. Enabling it will force the game into the above described idle mode.                                                         	| UR_IDLE           	|
| FR_TIMER             	| To ensure the scenario game mode doesn’t go on for too long, there will be a clear timer that the user can always see for time management                                                     	| UR_GAMEMODES      	|

# Non-Functional Requirements
| ID                   	| Description                                                                                        	| User Requirements         	| Fit Criteria                                                                         	|
|----------------------	|----------------------------------------------------------------------------------------------------	|---------------------------	|--------------------------------------------------------------------------------------	|
| NFR_MOVE_ACCESSIBLE  	| The game should have basic controls that are intuitive and easy to learn.                          	| UR_MOVE, UR_ACCESSIBILITY 	| People of all ages and abilities should be able to move.                             	|
| NFR_GAME_SHORT       	| The game should be short as people will be playing it on the open-day                              	| UR_GAMEMODES              	| Scenario mode < 5 minutes                                                            	|
| NFR_CONTROL_RESPONDS 	| The response time should be real-time and instant.                                                 	| UR_MOVE                   	| The controls should have instance > 0.01 seconds                                     	|
| NFR_STACKING_ITEMS   	| The items should be able to be stacked in any order.                                               	| UR_RECIPES                	| Prepped ingredients need to be present.                                              	|
| NFR_COOKING_TIME     	| Chopping and cooking should be completed in reasonable time.                                       	| UR_INTERACT               	| Takes > 5 seconds                                                                    	|
| NFR_CUSTOMER_DEMAND  	| Must allow for enough time to complete the recipe.                                                 	| UR_CUSTOMER               	| Demand > 60 seconds                                                                  	|
| NFR_SWITCH           	| Switching must be fast and responsive.                                                             	| UR_SWITCH                 	| Only slight cooldown time < 1 second                                                 	|
| NFR_WAITING          	| The game must provide an easy way of seeing recipe requests and the time left to complete.         	| UR_CUSTOMER               	| Have a bar telling which customers have ordered and the remaining time per order     	|
| NFR_AUDIO_CUES       	| The game should have audio cues on actions that are relevant and recognisable.                     	| UR_COOKS_INTERACT         	| Audio will make the game more engaging and serve as additional confirmation.         	|
| NFR_ENGAMENT         	| It should be fun and easy to play.                                                                 	| UR_GAMEMODES              	| The game should be engaging for all users                                            	|
| NFR_DIFFICULTY       	| The game should be easy to pick up and play by anyone regardless of how much experience they have. 	| UR_GAMEMODES              	| Ensure people can understand how to play regardless of age, experience and language. 	|
| NFR_ACCESSIBILITY    	| The game must be designed with the fact that it’ll be played in a busy environment.                	| UR_ACCESSIBILITY          	| The game must not rely on one identifier too much, such as sound, colour or text.    	|

# Constraint Requirements
* Stakeholder: The University of York Communications Office
* Customers: Lectures
* All software use must be open source and free
* Must be made in Java
* Should run on any desktop PC

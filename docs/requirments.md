# This is are requirments page

It seems to be a quiet day at the Piazza: there aren't that many students and staff around 
this time of the year, so most of the kitchen staff are away on leave - you only have three
cooks. Suddenly, a crowd bursts into the restaurant: it's an open day, and they all want to eat
at once! Make the most of your kitchen and your staff, and face up to the challenge of
serving an impatient and demanding crowd!

This is a single player game that requires managing staff around the a busy kitchen, who will be preparing
various dishes requested by customers coming to the Piazza Resturent Restaurant.


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 1; ALERTS: 0.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p>
<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>



# Requirements


# User Requirements


<table>
  <tr>
   <td>ID
   </td>
   <td>Description
   </td>
   <td>Priority
   </td>
  </tr>
  <tr>
   <td>UR_COOKS_MOVE
   </td>
   <td>Cooks must have the ability to move.
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_COOKS_SWITCH
   </td>
   <td>Must have the ability to switch between cooks.
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_COOKS_INTERACT
   </td>
   <td>Must have the ability to chop vegetables, flip items on the stove, grab and place items.
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_CUSTOMERS
   </td>
   <td>Customers must arrive and have a timer which will go down slowly, it dish is not severed in time then demand score is decremented 
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_GAMEMODES
   </td>
   <td>A scenario game mode where configurable number customers arrive and they have to be served in their time limit, must have some remaining reputation points to complete.
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_STATIONS
   </td>
   <td>Must have areas where cooks are able to chop raw vegetables, cook and flip patties, bake raw ingredients, serving, picking up ingredients and a counter for customers to wait.
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_RECIPES
   </td>
   <td>This recipes for salad, burger, pizza and jacket potatoes
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>UR_SHOP
   </td>
   <td>A menu where after the game is over cooks can invest money into buying other stations and unlocking recipes. Also they will be able to call other cooking staff back from leave
   </td>
   <td>Low
   </td>
  </tr>
</table>



# 


# Functional Requirements

Cooldown after switching cooks?

How do cooks get money?


<table>
  <tr>
   <td>ID
   </td>
   <td>Description 
   </td>
   <td>User Requirements
   </td>
  </tr>
  <tr>
   <td>FR_COOKS_MOVEMENT
   </td>
   <td>The cooks will move up, down, left, right with given the input using a keyboard
   </td>
   <td>UR_COOKS_MOVE
   </td>
  </tr>
  <tr>
   <td>FR_COOKS_SWITCH
   </td>
   <td>The user will be able to switch cooks by pressing a key
   </td>
   <td>UR_COOKS_SWITCH
   </td>
  </tr>
  <tr>
   <td>FR_COOKS_FLIP
   </td>
   <td>Must have the ability to flip items on the stove. This must be done before patty burns.
   </td>
   <td>UR_COOKS_INTERACT
   </td>
  </tr>
  <tr>
   <td>FR_COOKS_GRAB
   </td>
   <td>Cooks must be able to grab items.
   </td>
   <td>UR_COOKS_INTERACT
   </td>
  </tr>
  <tr>
   <td>FR_COOKS_PLACE
   </td>
   <td>Cooks must be able to place items down after picking them up.
   </td>
   <td>UR_COOKS_INTERACT
   </td>
  </tr>
  <tr>
   <td>FR_CUSTOMER_ARRIVE
   </td>
   <td>Customers arrive at random time intervals and request a recipe with a dialog box that includes the required ingredients.
   </td>
   <td>UR_CUSTOMER_ARRIVE
   </td>
  </tr>
  <tr>
   <td>FR_GAMEMODE_1
   </td>
   <td>A scenario game mode where configurable number customers arrive and they have to be served in their time limit, must have some remaining reputation points to complete.
   </td>
   <td>UR_GAMEMODES
   </td>
  </tr>
  <tr>
   <td>FR_GAMEMODE_2
   </td>
   <td>A “endless” game mode where customers will arrive until all reputation points are lost. The number of customers served before all points are lost is the score.
   </td>
   <td>UR_GAMEMODES
   </td>
  </tr>
  <tr>
   <td>FR_COOKING_STATION_1
   </td>
   <td>Must have an area where cooks are able to chop raw vegetables. If vegetables are not cut well enough must be discarded
   </td>
   <td>UR_STATIONS
   </td>
  </tr>
  <tr>
   <td>FR_COOKING_STATION_2
   </td>
   <td>Must have an area where cooks are able to cook and flip patties, this needs to be completed in a time limit otherwise patties will burn and they have to be discarded.
   </td>
   <td>UR_STATIONS
   </td>
  </tr>
  <tr>
   <td>FR_COOKING_STATION_3
   </td>
   <td>This is the baking section where cooks are able to bake raw ingredients
   </td>
   <td>UR_STATIONS
   </td>
  </tr>
  <tr>
   <td>FR_SERVING_STATION
   </td>
   <td>This is an area where cooks can place the made recipes and customers can receive their order
   </td>
   <td>UR_STATIONS
   </td>
  </tr>
  <tr>
   <td>FR_INGRIDENT_STATION
   </td>
   <td>This is an area where cooks can can pick up raw ingredients to prepare, these will automatically regenerated and cooks can pick up multiple
   </td>
   <td>UR_STATIONS
   </td>
  </tr>
  <tr>
   <td>FR_COUNTER
   </td>
   <td>This is an area where the customers will wait for their order.
   </td>
   <td>UR_STATIONS
   </td>
  </tr>
  <tr>
   <td>FR_RECIPE_1
   </td>
   <td>This recipe is the salad and contains: chopped lettuce, chopped tomatoes and chopped onions. These must be stacked on a plate.
   </td>
   <td>UR_RECIPES
   </td>
  </tr>
  <tr>
   <td>FR_RECIPE_2
   </td>
   <td>This recipe is the burger and contains: fried patty (must be formed first), a toasted bun. These must be stacked on a plate.
   </td>
   <td>UR_RECIPES
   </td>
  </tr>
  <tr>
   <td>FR_RECIPE_3
   </td>
   <td>This recipe is a pizza and contains: a base, a sauce, a topping all stacked and then cooked.
   </td>
   <td>UR_RECIPES
   </td>
  </tr>
  <tr>
   <td>FR_RECIPE_4
   </td>
   <td>This recipe is a jacket potato containing: a cooked potato and a topping stacked on a plate.
   </td>
   <td>UR_RECIPES
   </td>
  </tr>
  <tr>
   <td>FR_SCORE
   </td>
   <td>This is a variable that is initially 3 and when a demand is not met it will decrement 
   </td>
   <td>UR_CUSTOMER
   </td>
  </tr>
  <tr>
   <td>FR_CUSTOMER_ARRIVE
   </td>
   <td>Customers will arrive at a given random time interval. They will initial arrive on their own then in groups
   </td>
   <td>UR_CUSTOMER
   </td>
  </tr>
  <tr>
   <td>FR_CUSTOMER_DEMAND
   </td>
   <td>When a customer arrives they will request an item and give a time limit.
   </td>
   <td>UR_CUSTOMER
   </td>
  </tr>
  <tr>
   <td>FR_MONEY
   </td>
   <td>This is a score when a customer is served within the time frame the player will be rewarded some money.
   </td>
   <td>UR_SHOP
   </td>
  </tr>
  <tr>
   <td>FR_SHOP_MENU
   </td>
   <td>This is menu where the player can spend coins on more stations and cooks
   </td>
   <td>UR_SHOP
   </td>
  </tr>
</table>



# 


# Non-Functional Requirements



* How long should each game last?
* What difficulty level should be?
* What is the time limit for waiting customers?
* How long should items take to cook?
* Should recipes be displayed?
* What sort of movement? speed, direction?
* Can you stack raw items?

<table>
  <tr>
   <td>
ID
   </td>
   <td>Description
   </td>
   <td>User Requirements
   </td>
   <td>Fit Criteria
   </td>
  </tr>
  <tr>
   <td>NFR_MOVE_ACCESSIBLE
   </td>
   <td>The game should have basic controls that are easy to learn.
   </td>
   <td>UR_MOVE
   </td>
   <td>All ages and abilities should be able to move
   </td>
  </tr>
  <tr>
   <td>NFR_CONTROL_RESPONDS
   </td>
   <td>The response time should be real-time and instant.
   </td>
   <td>UR_MOVE
   </td>
   <td>The controls should have instance >0.01 seconds
   </td>
  </tr>
  <tr>
   <td>NFR_STACKING_ITEMS
   </td>
   <td>The items should be able to be stacked in any order.
   </td>
   <td>UR_RECIPES
   </td>
   <td>Prepped ingredients need to be present
   </td>
  </tr>
  <tr>
   <td>NFR_COOKING_TIME
   </td>
   <td>Chopping and cooking should be completed in reasonable time.
   </td>
   <td>UR_STATIONS
   </td>
   <td>Takes >5 seconds
   </td>
  </tr>
  <tr>
   <td>NFR_CUSTOMER_DEMAND
   </td>
   <td>Must allow for enough time to complete recipe 
   </td>
   <td>UR_CUSTOMER
   </td>
   <td>Demand >60 seconds
   </td>
  </tr>
  <tr>
   <td>NFR_SWITCH
   </td>
   <td>Switching must be fast and responsive
   </td>
   <td>UR_SWITCH
   </td>
   <td>Only slight cooldown time 1 second
   </td>
  </tr>
</table>



# Constraint Requirements



* Stakeholder: The University of York Communications Office
* Customers: Lectures
* All software use must be open source and free
* Must be made in Java
* What kind of systems should it run on?
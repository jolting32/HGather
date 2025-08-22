# HGather
This is a simple Digging / HELM / Farm / Fish tracker for FFXI. This addon works with Ashita v4. 

## HELM
In order to handle HELM macros that rely on <lastst> the addon defaults to whatever HELM activity you have active in the addon if it can not determine what type of target resource you are farming.

Example macro page:
```
/item "Pickaxe" <stnpc> <wait5>
/item "Pickaxe <lastst> <wait5>
/item "Pickaxe <lastst> <wait5>
/item "Pickaxe <lastst> <wait5>
/item "Pickaxe <lastst> <wait5>
/item "Pickaxe <lastst> <wait5>
```

## Farm / Fish
Currently experimental, enable through the /hgather settings as "Hunt" and "Fish" modes.

## Commands
/hgather or /hgather editor - Opens the configuration menu

/hgather show/hide - Shows or hides the addon window

/hgather update - Updates the pricing for items based on what you entered in your settings

/hgather report - Prints the dig data to chatlog (only dig data currently)

/hgather clear - Clears the hgather session data

## Pricing
Pricing for items is listed under the configuration window under the Items tab. Make sure the format is as follows:

**Format**: item name:itemprice

**Example:** pebble:100

This would price pebbles at 100g.

If you update the prices while in game, make sure to use the **/hgather update** command to update the prices.

## Updates 
August 22, 2025
- Added an inventory count to all the tabs.
	- This is useful to allow you to see how many spots you have left in your inventory.

August 21, 2025
- Updated the hunt tab to include the weather.
    - This is useful for farming elementals in a zone. This is turned on by the weather display checkbox in the menu.

August 12, 2025
- Updated the item list for the tracker.
	- Added more items to the list that were not there before. 
- Added a check box to always keep Hgather open
	- This is an optional check box to always keep it open. Checking the box will also check the visible option as well.
- The list automatically sort by alphabetical order.
	- All the list will not display items in alphabetical order. 

June 13, 2025
- Removed the hunt percentage as it broke the Addon and it is not needed.
	- This is not in the Hunt tab as you may kill different mobs and the results will not be accurate.	

June 12, 2025
- Changed the variables for the chat to monitor.
	- This fixed it to where certain items would never be counted because of the wording. The problem existed when it was matching the message wording.
- Moved the variables outside of the if statement to capture the text before the if statement. 
	- This fixed the issue to where the count would not be exact. The problem was if a different message came in right after the item was gotten, it would take the new message instead of the intended message.
- Added a percentage to the break counter for mining.  
	- This enhances the addon to show how often breaks will happen. 
- Added in percentage to all items gathered.
	- This enhances the addon to show how likely you are to get an item. 
- Updated the item list for the tracker.
	- Added more items to the list that were not there before. 
- Cleaned up the code a little due to the changes that were made. 
	- I removed several things from the addon that were redundant after the changes that were implemented.
	



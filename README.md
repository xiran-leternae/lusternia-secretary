# Version
alpha 

# Install
Download the raw of FairySec.xml. In Mudlet, select Packages and Install New Package.

# Syntax
```
FAIRYSEC INSTRUCTIONS - instructions for manually gathering logs
FAIRYSEC RESET	- reset gathered logs
FAIRYSEC REVIEW	- show the gathered logs
FAIRYSEC SAVE	- save the gathered logs to a file
FAIRYSEC REPORT [<person>|ALL] [FOR <year> CE WITH <orgCredits> CREDITS]
	- show tally for org member or all of the org

FAIRYSEC ADD [timestamp] [uniqueAppend] (<type>) <desc>: <names>
FAIRYSEC UPDATE <timestamp> [uniqueAppend] (<type>) <desc>: <names>
FAIRYSEC DELETE <timestamp> [uniqueAppend] (<type>)
	- modify log entries. Timestamp must be in format yyyy/mm/dd hh:mm:ss for GMT.
If adding a log entry, it defaults to the current GMT time.
```

# Instructions
Note: If not already done, configure org-specific variables under 'fairySec variables' > 'org specific'
1. Manually enable trigger group 'fairySec tracking'
2. Read logs. There is an alias to help with this.
`SEARCHLOG <log name> <start weave> <end weave> [query]`, Ex.
```
SEARCHLOG SERENWILDE 21 8 timequake
```
3. Manually disable trigger group 'fairySec tracking' when done
4. `FAIRYSEC REVIEW` and modify log entries as needed. Ex.
```
FAIRYSEC ADD 2023/10/01 22:31:48 (otherConquest) Wild Nodes: Jolanthe, Madungonga, Galaphyrae, Huskii, Xiran
```
5. `FAIRYSEC REPORT FOR <year> CE WITH <orgCredits> CREDITS`, Ex.
```
FAIRYSEC REPORT FOR 659 CE WITH 600 CREDITS
```

# Customisation
The configuration of credit rewards per activity can be found in 'fairySec variables' > 'org specific'
```
fairySec.rewards = {
  ["timequake"] = 3, -- 3 credits per timequake
  ["domoth"] = 5, -- 5 credits per domoth, and so on
  ["revolt"] = 5,
  ["aetherflare"] = 5,
  ["otherConquest"] = 5,
  ["design"] = 15,
  ["prestige"] = 60,
  ["empower"] = 10, -- empowering the Aspects/Elemental Lords
```
Player-logged activities, such as revolts, aetherflares, and wild nodes will require triggers set up to match your organisation. Power contributions will also require triggers set up. 

The display for the report may be customised (ex. default code has `domoth`, `revolt`, `aetherflare`, and `otherConquest` all grouped under the label "Conquest") by changing the code.

Custom formulas for rewards (ex. default code has a library reward of book weight * 4 credits) can also be done in the code.

* To update searching through logs, edit Triggers under Fairy Secretary.
* To update display for the report, edit Scripts: 'fairySec print functions' and org specific variables.
* To update rewards, edit Scripts: 'fairySec tally functions' and org specific variables.

# Contact Support
Xiran can be reached via the official Lusternia Discord or at the Lusternia Forums. Thank you!

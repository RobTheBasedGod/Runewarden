# Runewarden
Runewarden Scripts

Runewarden Attack Freamework
-----------------------------

    This is just a framework for a way to handle all of your venom selections. Note, this is not a complete work, it will work as it         sits, but you need to add things and change things, this just shows you how to work it all in. I'll briefly go over the script, part     by part.
    
          The Lists
         -----------
         
         venomlist:
            This list is how we translate between the affliction names that AK Tracker deals with, and the actual venom we are going to             use to give said afflictions. Each time you add a new affliction into the scenario, you must add the affliction name and the             name of the venom that gives the affliction to this list. Use the same format as you see in the script. Make sure you add a             "," to the end of all entries except the very last one.
            
         venoms:
            This is the list where we will set our thresholds of where we want to re-apply the affliction based on how sure AK is that               they haven't cure the affliction yet. I suggest keeping curare at 100 since we always want to hit with it unless they didn't             cure it before the next attack. The rest of these you need to play with and find that sweet spot for your plan of attack.  
            
         venomprio:
            This is where we set the priority of what we want to afflict with. This is your bread and butter here and don't be afraid to             make new prio lists for different affliction routes. What is there already is kinda sporatic, but essentially a kelp stack.             You can have as many prio lists as you want, just follow the same format that I used.
            
         The Functions
        ---------------
        
          venom_pick()
              This simply picks our venoms for us. It will run down the priority list and check each entry against the threshold we set               up and it will add the first two that meet the criteria to the myvenoms list, stopping at 2 venoms. 
              
          runie_hit()
              Here is where we make our actual attack. The first thing it does is convert the afflictions in myvenoms into actual venom               names by referencing the venomlist list, then it will stand, wipe your scimitars, wield them, then rsl. If you ever                     upgrade or change your weapons, be sure to change the values of weapon1 and weapon2 that are at the very top of this                     script.
        
                

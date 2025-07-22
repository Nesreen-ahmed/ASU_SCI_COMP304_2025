# :mag_right: Scanner

> [!NOTE]
> Please, read these files as they are without any changes!

  > "If these files have spaces between words, read them as they are. Simply modify your code!"

> [!NOTE]
> Solve problems one by one, don't try to solve them all at once.
### Test Cases
  1. `(1,2),(1,red), (4,2),(5,green),(3,yellow)`
       > In this case the scanner should give an error because there is no **space** in our language (Automaton)!
       > But the scanner will still be able to understand the graph input if it ignores this **space**, so you need to modify your code to ignore the space if it is found!
       
  2. `(1,2),(1,red),(34,2),(25,green),(3,yellow)`
       > Make sure that this entry should consider that `34` is a number and not `3` is a number and `4` is a number.
       > NOTE!
       > `(1,2),(1,red),(34,2),(2 5,green),(3,yellow)` If we have this input, the scanner should print <NUMBER, 25> and not <NUMBER, 2> <NUMBER, 5> and not <NUMBER, 2 5>.
       
        
  3. `(1,2),(1,red),(34,2),(25,green),(3,yello`
        > Make sure this entry should give an error!  

> [!IMPORTANT]
> Please, write your own code!
> write your own code!
> Write your own code!

> [!IMPORTANT]
> You don't need to write the Doctors's code, your code must be unique from anyone else's "your Doctors, your friends" - just your own code!
> I expect to read 20 different codes in the next lab. go ahead! :muscle:

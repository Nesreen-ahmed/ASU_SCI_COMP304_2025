# :mag_right: Scanner

> [!NOTE]
> Please, read these files as they are without any changes!

  > "If these files have spaces between words, read them as they are. Simply modify your code!"

> [!NOTE]
> Solve problems one by one, don't try to solve them all at once.
### Test Cases

  1. `int intx int1 intint int iint = 34310 ;`
     
       > What if **space** is a Final State (space is a Token), that means we have a transition like `q0   q5`.  
       
  > [!TIP]
  > Remember that our case is that we have one space as a character, i.e. the case `q0           q5` is not our case.. we just have one space!
       
  > [!TIP]
  > Solve the problem in the simplest way to deal with this situation. I don't need a professional method!!

  > [!TIP]
  > Just write your own function to separate your transition function file.

  > [!NOTE]
  > Remember that your code should handle both cases of whether the space is Final or not automatically without any changes to your code! 

       
  2. `int intx int1 intint int iint = 34310 ;`
       > Make sure that this entry should consider that `int` is **INT**, `intx` is **VARIABLE** and not `int` is **INT** and `x` is **Variable**.

       
  3. Make sure to print your code with its own string like this: `<VARIABLE, intx >`

     
  4. Modify our Language
      - ADD q9 and  q10 to all states in automaton file.
      - ADD q10 to final states in automaton file.
      - ADD these transitions  **q3 _ q9**, **q9 t q10** to transitions file.
      - ADD this token **q10 INT_t** to tokens file.
      - Then test this input `int_t intx int1 intint int iint = 34310 ;`
        > must be considere `int_t` is **INT_t** not `int` is **INT** and `_` is **ERROR**.
  

> [!IMPORTANT]
> Please, write your own code!
> write your own code!
> Write your own code!

> [!IMPORTANT]
> You don't need to write the Doctors's code, your code must be unique from anyone else's "your Doctors, your friends" - just your own code!
> I expect to read 20 different codes in the next lab. go ahead! :muscle:

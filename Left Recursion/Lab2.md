# Compiler Lab2 : LL1 Grammar | `Eliminate Left Recursion`

## :repeat: Direct Left Recursion

    Direct left recursion occurs when a production rule's leftmost symbol on the right-hand side is the same nonterminal as the left-hand side.

    Example:
      S -> S a | S b | c | d
   ### ❓ How Eliminate Direct Left Recursion?!

    Using previous example : S -> S a | S b | c | d

    S -> c S' | d S'
    S' -> a S' | b S' | eps

    ❓What do you need to implement this method in c++?
         ➡️First, we need to read the grammar from the input file and store it in a suitable data structure.
         ➡️Second, we need to know which rules have and which do not have left recursion.
         ➡️Third, update the rules according to the previous step.

     ✅Finally, we need three functions `read()`, `hasRecursionOrNot()`, `update()`.

   ### ▶️ Test These Examples:
  
       1️⃣ S -> S a | S b | c | d
       
          ✅ S -> c S' | d S'
              S' -> a S' | b S' | eps

       2️⃣ E -> E + T | T
           T -> T * F | F
           F -> ( E ) | id 

           ✅  E -> T E'
                E' -> +T E' | eps
                T -> F T'
                T' -> *F T' | eps
                F -> (E) | id

## :repeat: InDirect Left Recursion

  Indirect left recursion occurs when a nonterminal can derive itself through a sequence of one or more intermediate nonterminals.

  Example:
    A -> B a | a
    B -> C b | b
    C -> A c | c
### ❓ How Eliminate InDirect Left Recursion?!

  Using previous example : 
    A -> B a | a
    B -> C b | b
    C -> A c | c

    First Step:
      A -> B a | a
      B -> C b | b
      C -> B a c | a c | c
      
    Second Step:
      A -> B a | a
      B -> C b | b
      C -> C b a c | b a c | a c | c
      There is a direct left recursion!

    Third Step:
        A -> B a | a
        B -> C b | b
        C -> b a c C' | a c C' | c C'
        C' -> b a c C' | eps
        
  ❓ What do you need to implement this method in c++?
  
       ➡️First, we need to read the grammar from the input file and store it in a suitable data structure.
       
       ➡️Second, we need to compare each pair of non-terminals with each other, and check if any rule leads to the left iteration. When it leads to it, you need to replace it with all the production rules.
            `Ex:` using previous Example
            
              1️⃣ compare (B, A) for all B productions (C b | b), there is no rule has `A` then there is no rule that leads to left recursion.
              
              2️⃣ Compare (C, A) For all C productions (A c | c), there is a rule for it `A` so there is a left recursion, so we need to replace A for all its production rules: C -> B a c | a c | c Now we need to update the grammar with this rule and continue.
    
              3️⃣  Compare (C, B) for all C productions (B a c | a c | c), there is a rule has `B` so there is a left recursion, So we need to replace B for all its production rules: C -> C b a c | b a c | a c | c Now we need to update the grammar with this rule and continue.
    
       ➡️Check if there is a direct left recursion using previous problem and remove it.

   ✅Finally, Notice well that the order of the non-terminals important, and removeing Indirect recursion may lead to direct recursion.

   >[!IMPORTANT]
   > You can actually write your own algorithm, and I believe there is another algorithm to solve this problem. Feel free to think of another way💪.

### ▶️ Test These Examples:

       1️⃣  A -> B a | a
            B -> C b | b
            C -> A c | c
       
          ✅ A -> Ba | a
              B -> Cb | b
              C -> cC' | acC' | bacC'
              C' -> bacC' | eps
  
       2️⃣ Exam Example 
         - A -> B a
         - B -> d a b | D b
         - D -> c B | A c
  
           ✅  ???
       

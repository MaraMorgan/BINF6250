# Introduction
Description of the project

# Pseudocode
Put pseudocode in this box:

```
1. build_markov_model (markov_model, new_text, order)
    Inputs:
     markov model - Dictionary of Dictionary containing words and count.
     new_text -  string of text
     order -  Order of the markov model
    Output:
     markov_model with updated counts from new_text

    1. split new_text into words
    2. Add N order of copies of the state *S*, start of the sequence.
    3. At the End of list, add one copy of *E* to mark end.
    4. Use sliding frame approach, the current state as the group of order words starting at position i. The next word as the word at position i + order. 
    5. Update the model with each observed transition:
        a. Never encountered current state, add it to the model with a new inner dictionary the `{next_word : 1}`
        b. if the current state exists in model, but the next word does not, then add only next word to inner dictionary with count 1.
        c. if both current state and next word exists, only increment the count. 
    6. Return markov_model

2. get_next_word(current_word, markov_model, seed)
    Inputs:
     current word - present state, a single word or tuple depending on state.
     markov model - trained model dict of dict produced by build_markov_model
     seed - testing and reproudcibility
    Outputs:
     A single word selected based on observed transition. 
    
    1. Use current_word as key in markov_model to get list next word and counts
    2. From inner dictionary, build two list, one is list of possible words and other is list of counts
    3. Convert the counts to probabilities. 
    4. Return the chosen the word based on probabilities. 
    
```

# Successes
Description of the team's learning points

# Struggles
Description of the stumbling blocks the team experienced

# Personal Reflections
## Group Leader
Group leader's reflection on the project

## Other member
Other members' reflections on the project

# Generative AI Appendix
As per the syllabus

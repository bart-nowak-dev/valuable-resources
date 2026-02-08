# DDD - Domain Driven Design notes
## Object Oriented Programming principles - nice explenation:
+ **Abstraction**: The object is an agent that receives signals
+ **Encapsulation**: Hidden the way how signal is handled
+ **Polymoprhism**: Behavioral variations handle with separate types 
+ **Inheritance**: Bahvior which supports polymorphism  
**Fun fact**: Alan Kays said he should name this paradigm Message Oriented Programming instead of Object Oriented Programming.

## Programming paradigms - when to use which:
+ **Object oriented**: Stable behaviors/signals, unstable data structure
+ **Procedural**: Stable data structure, unstable procedures/services

## System/Objects modeling: 
1. **Being(Structural)**:
   * What is the structure of the thing?
   * Too many business questions can't be asked when we're modeling being (e.g. How many elements can be there?)
   * Pseudo behavior:  
     "Given a given product that is priced in price list X," inputs that there will be a product table and a price column there. i.e., data structures.
     "Teachers have many courses, the course consists of modules, the student has many courses"
     "Courses are visible when their status is X"
2. **Behaving**:
   * How it behaves
   * How it responds to signals:
   * Can the responses/reactions be repeated/reversible?
   * **IMPORTANT QUESTIONS YOU CAN ASK**:  
     * What changes?
     * How often does it change?
     * Why does it change?
     * Under what conditions does it change?
     * Who changes?
     * How frequently it change?
   * Rephrased example from Being modeling:  
     "Having a situation where the owner has priced the product at X, when"
     "Only board members can approve the prices
3. **Becoming**:
   * How it turns into something else
# Aggregates
**What is an aggregate?**  
The aggregate encapsulates those rules that must be consistent immediately.  
**_Recommended book: Rethinking systems analysis & design gerald m. weinberg_**

# 3 types of coupling(Google 3C):
1. **Create**
   * Meaning one aggregate creates another aggregate and returns it. This is OK (e.g., Owner has been charged (owner.charge()) and the result is a payment, which is a new aggregate).
2. **Contain**
   * **PROHIBITED!** Meaning I have a reference to another aggregate within me.
3. **Call**
   * Meaning I am a call parameter (it's better to pass OwnerData instead of Owner, for example).

# 2 types of events:
1. Inside module - **BAD**
2. Outside module - **OK**

# How to implement aggregate:
* One public class: the aggregate root, a factory, interface, and a repository interface. All internal entities are non-public.
* Recommended book: "Enterprise And MDA Patterns". These are structural patterns, but they are so well thought out that adding behaving and becoming to them is easy.

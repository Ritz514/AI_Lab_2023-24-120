# Ex.No: 11  Planning –  Monkey Banana Problem
### DATE:  01-04-2024                                                                           
### REGISTER NUMBER : 212221040120
### AIM: 
To find the sequence of plan for Monkey Banana problem using PDDL Editor.
###  Algorithm:
Step 1:  Start the program <br> 
Step 2 : Create a domain for Monkey Banana Problem. <br> 
Step 3:  Create a domain by specifying predicates. <br> 
Step 4: Specify the actions GOTO, CLIMB, PUSH-BOX, GET-KNIFE, GRAB-BANANAS in Monkey Banana problem.<br>  
Step 5:   Define a problem for Monkey Banana problem.<br> 
Step 6:  Obtain the plan for given problem.<br> 
Step 7: Stop the program.<br> 
### Program:

(define (domain blocksworld)
(:requirements :strips :equality)
(:predicates (clear ?x)
(on-table ?x)
(arm-empty)
(holding ?x)
(on ?x ?y))
(:action pickup
:parameters (?ob)
:precondition (and (clear ?ob) (on-table ?ob) (arm-empty))
:effect (and (holding ?ob) (not (clear ?ob)) (not (on-table ?ob))
(not (arm-empty))))
(:action putdown
:parameters (?ob)
:precondition (and (holding ?ob))
:effect (and (clear ?ob) (arm-empty) (on-table ?ob)
(not (holding ?ob))))
(:action stack
:parameters (?ob ?underob)
:precondition (and (clear ?underob) (holding ?ob))
:effect (and (arm-empty) (clear ?ob) (on ?ob ?underob)
(not (clear ?underob)) (not (holding ?ob))))
(:action unstack
:parameters (?ob ?underob)
:precondition (and (on ?ob ?underob) (clear ?ob) (arm-empty))
:effect (and (holding ?ob) (clear ?underob)
(not (on ?ob ?underob)) (not (clear ?ob)) (not (arm-empty))))







### Input 
(define (problem pb1)
(:domain blocksworld)
(:objects a b)
(:init (on-table a) (on-table b) (clear a) (clear b) (arm-empty))
(:goal (and (on a b))))

### Output/Plan:

![324335016-684b4714-ee43-47d7-bf57-db6ac6e64416](https://github.com/Ritz514/AI_Lab_2023-24-120/assets/142646304/98178793-f122-4135-a3bb-d53da5e18591)


### Result:
Thus the plan was found for the initial and goal state of given problem.

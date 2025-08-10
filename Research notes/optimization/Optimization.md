
# Genetic Algorithm
Key words: #evolutionary_algorithm , #GA, #population_size, #mutation_fraction, #crossover_fraction 
its a *search optimization technique* that adopts the theory of natural selection. 
A type of #evolutionary_algorithm 
principles of genetics and natural selection to solve complex problems.
Working principle:
It generates a set of potential solutions--> the population generated is evaluated--> the fittest individuals are selected and recombined with other populations to test new solutions. --> and the cycle repeates.


NSGA

![[Pasted image 20250115053416.png]]




Mind map
Memory Palace for Learning NSGA-II (Non-Dominated Sorting Genetic Algorithm II)

We'll map each major concept of NSGA-II to a location in my apartment. The key is to create vivid, exaggerated mental images are crucial to making recall easier.

Step 1: Assigning NSGA-II Concepts to Locations

|                                             |                          |                                                                                                                                                                                                                                         |
| ------------------------------------------- | ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NSGA-II Step                                | Apartment Location       | Crazy Mental Image                                                                                                                                                                                                                      |
| 1. Initialize Population                    | Door                     | You open the door and a crowd of tiny electric cars rushes in, each shouting their specs ("Wheel size: 18 inches! Battery: 80 kWh!"). This represents generating the initial population.                                                |
| 2. Evaluate Fitness                         | Stairs & Entryway Closet | A scientist at the stairs is testing each tiny car, recording its acceleration time and range on a clipboard. Some cars zoom up the stairs, others stall halfway—visualizing fitness evaluation.                                        |
| 3. Generate Offspring                       | Living Room              | In the middle of the room, two cars are having a robotic wedding, where a mechanical arm mixes their features (Crossover). A mad scientist in a lab coat zaps cars with a mutation ray, making some grow huge batteries or tiny wheels! |
| 4. Combine Populations                      | Kitchen (Fridge)         | You open the fridge, and the old and new cars are stacked inside like groceries. They are getting sorted for freshness, just like the parent and offspring populations being merged.                                                    |
| 5. Rank Individuals (Non-Dominated Sorting) | Microwave                | Inside the microwave, tiny cars are forming queues labeled "Front 1," "Front 2," etc. The best cars (Front 1) are at the top, ready to leave, while others wait below—representing sorting by Pareto dominance.                         |
| 6. Select New Population                    | Burner (Stove)           | The best cars are jumping onto the stove, getting "cooked" into the next generation. Some get rejected and fall off because of their crowding distance score, ensuring diversity.                                                       |
| 7. Stopping Criteria                        | Dining Table             | At the dining table, a judge with a stopwatch announces: "Stop! We've reached 100 generations!" or "No more improvement, we're done!"—visualizing the algorithm’s stopping conditions.                                                  |

Step 2: Mapping Key NSGA-II Mechanisms to Additional Locations

|   |   |   |
|---|---|---|
|NSGA-II Mechanism|Location|Mental Image|
|Non-Dominated Sorting|Toilet|Inside the toilet, cars are trying to flush each other away! The strongest ones refuse to go down, staying at the top (Front 1), while weaker ones (dominated solutions) spiral downward.|
|Crowding Distance|Window|Outside the window, cars are pushing each other for space—some are closer, others spread out, representing diversity maintenance.|
|Tournament Selection|Coat Closet|Inside the closet, two cars are wrestling—the stronger one wins and moves forward (higher rank), but if they’re equal, the one with more space (crowding distance) wins.|
|Crossover|Oven|Inside the oven, two half-melted cars fuse together, one car getting the wheels of the other, representing genetic combination.|
|Mutation|Toilet Paper Roll|A scientist is scribbling new random features on toilet paper, modifying the car designs just like mutation introduces random variations.|

Step 3: Practicing Your Memory Palace

1. Mentally walk through your apartment and recall the images at each location.
2. Connect the images to the NSGA-II steps/mechanisms.
3. Test yourself: Try recalling the entire NSGA-II process without looking at the notes.
4. Refine the story: The funnier, crazier, and more emotional your images, the better they will stick!

Why This Works

✅ Uses spatial memory → Your apartment layout is already mapped in your brain.

✅ Engages visual & emotional memory → Wild, exaggerated images are easier to recall.

✅ Breaks complex ideas into simple, memorable parts → You don’t need to remember raw definitions, just the scenes, which bring back the concepts.

Would you like to add more details, or would you prefer another process to practice? 😊🚀

From <[https://chatgpt.com/g/g-GaK0nIsQY-study-notes/c/679bb33f-b7f4-800c-b7d6-2285db026beb](https://chatgpt.com/g/g-GaK0nIsQY-study-notes/c/679bb33f-b7f4-800c-b7d6-2285db026beb)>





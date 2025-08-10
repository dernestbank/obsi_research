Particle swarm Optimiztion

Particle Swarm Optimization was proposed in 1995 by Kennedy and Eberhart [22] based on the simulating of social behavior. It is inspired by the social behavior of bird flocking or fish schooling. The algorithm uses a swarm of particles to guide its search. Each particle has a velocity and is influenced by locally and globally best-found solutions. 

```python
import numpy as np

def fitness_function(position):
    return sum(x**2 for x in position)

def update_velocity(particle, global_best_position, w=0.5, c1=1, c2=2):
    r1, r2 = np.random.rand(2)
    
    cognitive_velocity = c1 * r1 * (particle['best_position'] - particle['position'])
    social_velocity = c2 * r2 * (global_best_position - particle['position'])
    
    particle['velocity'] = w * particle['velocity'] + cognitive_velocity + social_velocity

def update_position(particle, bounds):
   
    particle['position'] = particle['position'] + particle['velocity']
    particle['position'] = np.clip(particle['position'], bounds[0], bounds[1])

def initialize_swarm(num_particles, bounds, dimensions):
    swarm = []
    for _ in range(num_particles):
        particle = {
            'position': np.random.uniform(bounds[0], bounds[1], dimensions),
            'velocity': np.random.uniform(-1, 1, dimensions),
            'fitness': float('inf'),
            'best_position': None,
            'best_fitness': float('inf')
        }
        swarm.append(particle)
    return swarm

def pso(fitness_function, bounds, dimensions, num_particles=30, iterations=100):
    
    swarm = initialize_swarm(num_particles, bounds, dimensions)
    global_best_position = None
    global_best_fitness = float('inf')

    for _ in range(iterations):
        for particle in swarm:
           
            particle['fitness'] = fitness_function(particle['position'])

            if particle['fitness'] < particle['best_fitness']:
                particle['best_fitness'] = particle['fitness']
                particle['best_position'] = particle['position'].copy()

            if particle['fitness'] < global_best_fitness:
                global_best_fitness = particle['fitness']
                global_best_position = particle['position'].copy()

        for particle in swarm:
            update_velocity(particle, global_best_position)
            update_position(particle, bounds)
    return global_best_position, global_best_fitness

```


This code defines the basic components of a PSO algorithm:

- **Initialization**:
    
    The swarm is initialized with random positions and velocities within the search space.
    
- **Fitness Evaluation**:
    
    Each particle's position is evaluated using the fitness function.
    
- **Update Personal Best**:
    
    If a particle finds a better position, it updates its personal best position and fitness.
    
- **Update Global Best**:
    
    The best position found by any particle in the swarm is tracked as the global best.
    
- **Update Velocity and Position**:
    
    Each particle adjusts its velocity based on its personal best and the global best, and then updates its position.
    
- **Iteration**:
    
    Steps 2-5 are repeated for a set number of iterations or until a stopping criterion is met.


pymoo documentation [pymoo - PSO: Particle Swarm Optimization](https://pymoo.org/algorithms/soo/pso.html)]



-----


Genetic algorithms are a type of optimization algorithm inspired by the process of natural selection and evolution. They are used to find optimal or near-optimal solutions to complex problems.

initiation: potential solutions are generated as chromosome

evaluation: potential solutions are tested against the fitness function

selection: high-fitness chomosoms are more likely to be selected for reproduction( survival of the fittest)

crossover: selected chromosomes are recombined oto generate new set of offsprings 

mutation: occationally randoom changes are are introduced to create diversit in solutions

replacement: new offsprings are combined with some original population to create the next generation

Termination: the algo continues until a stopping criterion is met.


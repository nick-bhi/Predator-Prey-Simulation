# Predator-Prey-Simulation
This program simulates an extremely simplified ecosystem of herbivores and carnivores. The herbivores (blue cubes) eat the plants (green spheres) and the carnivores (red cubes) eat the herbivores. 
## Attributes
![Stats](https://raw.githubusercontent.com/nick-bhi/Predator-Prey-Simulation/master/Stats-Pic.JPG)

Each animal (herbivore and carnivore) has 4 attributes: size, speed, strength, and perception. Larger animals will burn more calories and give birth less frequently, but they also have a significant advantage in fights.
Speed determines how quickly an animal moves, but it also means they will burn more calories. Strength adds to an animal's fighting ability. While size has a more signficant impact in fights, more strength doesn't require more calories.
Lastly, perception determines an animal's range of perception for plants, carnivores, and herbivores. Higher perception requires more energy.
## AI Navigation
![Navigation](https://raw.githubusercontent.com/nick-bhi/Predator-Prey-Simulation/master/Simple%20Pred-Prey%20Pic.JPG)

Every frame update, each animal checks for all objects in its perception radius. It then chooses the closest object within that radius and acts accordingly. If the animal is an herbivore, it will orient itself towards food and away from a carnivore. If the animal is a carnivore, it will orient itself towards herbivores. If there are no relevant objects in an animal's perception radius, it will choose a random point in the environment and move towards that.
## Energy
Each animal is born with a set energy level. The starting energy level is determined by the size of the animal. Each frame, energy is deducted based on size, speed, and perception. When an herbivore eats a plant, it gains 500 energy. When a carnivore eats an herbivore, it gains however much energy the herbivore had before it died. If an animal's energy level gets to 0, it dies. Over time, herbivores and carnivores will evolve based on 
## Birth
Once an animal reaches double its starting energy and a certain amount of time has passed, it will give birth. Larger animals have a longer waiting period before they can give birth. The attributes of an animal's child will be within a random range of 1 of the original animal.  
## Fights
When a carnivore encounters an herbivore, the two will fight. An animal's total offensive score is the summation of its size and strength. The animal with the lower offensive score will die. The winning animal will lose energy depending on the difference between its own offensive score. Closer offensive scores will lead to more energy loss.
## Environment Initialization
![Field Settings](https://raw.githubusercontent.com/nick-bhi/Predator-Prey-Simulation/master/Field-Settings.JPG)

There are 5 environment settings that determine the starting conditions of the simulation:
* **# of Predators** - How many carnivores will spawn
* **# of Prey** - How many herbivores will spawn
* **# of Food** - How many plants will spawn
* **Food Spawn Time** - How often a new plant will spawn in miliseconds
* **Field Size** - The size of the environment

## Example Runs
https://www.youtube.com/watch?v=DtmfzWNYmQI

https://www.youtube.com/watch?v=KPll3BpO_yo

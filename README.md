# Submission

Name: Megan Reddy \
Partner: Joanna Fisch

# Puzzle 1 - Cell Mitosis

For this puzzle, I modified the **feed rate** to create a cellular mitosis effect.

**feed_rate = 0.028**

D_A = 1

D_B = 0.5

kill_rate = 0.0608

delta_time = 1

![Cell Mitosis GIF](cell_mitosis.gif)
![Cell Mitosis Image](cell_mitosis.PNG)

# Puzzle 2 - Equilibrium

I modified the **kill_rate** to create this equilibrium effect. The middle circles do not vary much between the 5th and 100th frames.

**kill_rate = 0.065**

D_A = 1

D_B = 0.5

feed_rate = 0.055

delta_time = 1

![Equilibrium GIF](equilibrium.gif)

Frame 5:

![Equilibrium Image](equilibrium_5.PNG)

Frame 100:

![Equilibrium Image](equilibrium_100.PNG)

# Puzzle 3 - Concentric Circles

For this effect, I lowered the diffusion rate of chemical B so that the simulation preserves the original location of the seeds. Notice how the concentric circle patterns surround the original positions of the seeds.

**D_B = 0.205**

D_A = 1

feed_rate = 0.055

kill_rate = 0.062

delta_time = 1

![Concentric GIF](concentric.gif)

Seed Placement:

![Concentric Image](concentric_seeds.PNG)

Frame 100:

![Concentric Image](concentric.PNG)

# Extra Tasks

## Disappearing Seeds

I used a VEX expression to modify the kill rate so that the seeds disappeared over time.

D_A = 0.4

D_B = 0.09

feed_rate = 0.075

kill_rate = sin(@Time) + 0.065

delta_time = 1

![Concentric Image](disappearing_squares.gif)

## Water Simulation

I used a VEX expression to vary the seed heights over time and played with a few of the other parameters (D_A, D_B, feed_rate, and kill_rate) to create this water-like animation.

VEX Expression for height:
```
float offset = 0.5 * (sin(5.0 * @Time) + 1.0) + 0.43;
@P.y = fit(f@A, 0, 1.0, height * offset, 0.0);
```
D_A = 0.67

D_B = 0.4

feed_rate = 0.0299

kill_rate = 0.0536

delta_time = 1

![Concentric Image](water_simulation.gif)

# Lab06 - Reaction Diffusion
Let's play with the parameters and setup of the reaction-diffusion equation to create cool effects. You may work with a partner for this lab. **Please choose 3 of the following 5 puzzles/tasks to complete this lab.** Additional puzzles/task may be completed for extra credit.

# Setup
Download and open Houdini with the ReactionDiffusionPlayground.hipc file found in this repository.

# Puzzle 1
Modify the **feed rate** to create a cell mitosis (cellular division) affect.

The other parameters will be as follows:

D_A = 1

D_B = 0.5

kill_rate = 0.0608

delta_time = 1


![image](https://user-images.githubusercontent.com/60444726/197622415-ca9b9623-d01b-4e54-9b1a-b79109248cab.png)


# Puzzle 2
Modify the **kill rate** to create an simulation that reaches equilibrium very quickly. The rings should be approximately where the starting seeds were, and there should be little change between the 5th and the 100th frame.

The other parameters will be as follows:

D_A = 1

D_B = 0.5

feed_rate = 0.055

delta_time = 1



![image](https://user-images.githubusercontent.com/60444726/197624737-58ab1aca-accb-4b4a-9654-cdc5fe84e723.png)

Frame 5


![image](https://user-images.githubusercontent.com/60444726/197624645-e5b13798-ae74-4e18-84dc-955a9919021c.png)

Frame 100

# Puzzle 3
Modify the diffusion rate of chemical B (D_B) to create a simulation that still demonstrates where the seeds were at the start of the algorithm. There should be parts of concentric circles surrounding each seed location. To see if you're on the right track, run the simulation and then check (or have a friend check) and see if you can idenitfy where all the seeds were at the start of the algorithm!

The other parameters will be as follows:

D_A = 1

feed_rate = 0.055

kill_rate = 0.062

delta_time = 1

![image](https://user-images.githubusercontent.com/60444726/197626261-1e4fa5d4-d9d8-4563-8b92-c2b2a20038f7.png)
Seed Placement

![image](https://user-images.githubusercontent.com/60444726/197626365-9a91a0d6-1e6f-4b0f-838b-7047c153d860.png)
Frame 100

# Task 1
Modify the shape, size, or placement of the seeds in the playground to create an interesting effect. Which node might you need to adjust? How can you change the exisitng VEX to create something interesting?

# Task 2
Modify some of the parameters to create a cool effect. This effect can be displayed with a video or image, depending on whether you want to showcase the animated effect or the algorithm's result.

# Submission
- Create a pull request to this repository
- In the README, include the names of both of your team members
- In the README, include a description of the task or puzzle you completed, screenshots/images (or videos!) of your results, AND the values for all the parameters you changed
- There is no need to upload a Houdini File. Screenshots of your results and images (or written values) of the parameters will be sufficient!

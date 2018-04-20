# Notes
## What Computational Physics is Really About
There are many ways to model physics in real life ways for us to understand. These include: A chart showing the transfers of energy as a block slides along a table, an equation for the gravitational force between two objects, a differential equation describing the motion of a mass on a spring, and a computer program that calculates the motion of a baseball with air resistance. These are many models and not all models have to be mathematical models.

When talking about computational physics some key points are that computers are very important and code can be ran to analyze data. This bridges both theory and experiment. We can use physics for like projectiles and springs to be models computationally. These can be plotted to so we have a visualization of them. Computational is where we do theoretical physics where we build models. 

## 12 Steps Toward Rock-Solid Scientific Python Code
Following these 12 steps will allow you to have confidence in your computer skills, accelerate and better communicate on the computer, and finally work better with others.

The first step is to use verion control. This helps by keeping steps and work ordered. Then put the code in the cloud so it can be reviewed and edited by peers. Add a README and a License so we can describe  to our audience the purpose of the code and they can exicute it. Make sure there are docstrings so people reading your code can understand it better. Other smaller steps are to write tests, keep track of issues, automate tests and the build, use continuous integration, monitor test coverage. Finally it is important to write narrative documentation so the audience is able to better understand the reason for every part of your project and also so peers and help find issues in your project.


# Other
 As far as projects go I plan on doing another project out of Giordano. I like his book most and the problems in them. One neat project would be the billiards problem, or another oscillatory problem. I may even look into different projectile motions not in the book.

# Outline
## General Idea
The general idea of the Billiard problem is that there is a ball that moves perfectly on a frictionless table. This means that the ball will move with a constant velocity when moving between the walls. We can assume the interactions with the walls are elastic, therefore there is no energy lost in the collision. Knowing all this and that the angle of reflection about the norm of the wall is equal, we can use Euler's Method to create a model of the balls trajectory.

The first of three concepts that will be tested is the Lyapunov of stadium tables that have been stretched a certain alpha. The second concept is to test different table shapes and initial conditions to pbserve how the trajectory is effected. The third concept to be tested is to use an exact equation for the velocity and solve the problem analytically.

## Controlling Equations
There are three sets of controlling equations. The first is the equations to describe the velocity of the ball between collisions with the walls. 

$\frac{dx}{dt} = v_{x}$ 


$\frac{dy}{dt} = v_{y}$

The second set of equations it to find the components of the veloctiy before it collides with the wall.


$\vec{v}_{i,\perp} = (\vec{v}_{i} \bullet \hat{n})\hat{n}$

$\vec{v}_{i,\parallel} = \vec{v}_{i} - \vec{v}_{i,\perp}$

The final set of equations is used to find the components of the velocity after the collision using the initial components.


$\vec{v}_{f,\perp} = -\vec{v}_{i,\perp}$

$\vec{v}_{f,\parallel} = \vec{v}_{i,\parallel}$

## Specific Scenerios
There are a few specific scenerios that will be
 tested in this problem. The first is to test the ball's trajectory due to a stadium table, and how changing the length of the sides, $\alpa$, change the ball's trajectory. The second scenerio the be tested is how an elliptical table will affect the trajectory of the billiard ball. If time permits a square table may also be tested. For all different tables, different initial conditions, such as velocity aand position will also be changed.

## Method
Euler's method will be used to model the trajectory of the billiard ball on the different tables. The collisions will be modelled by moving along the path of the ball and when it is off the table the program will go back to the point on the table and use steps approximately 100 times smaller and find the location of the edge. Using the location it will then use the equations for the velocity's components and find the velocity after the condition. This will be done for a set amount of time, and will create a trajectory to be modelled.

## Boundary Conditions
The boundary conditions for this project include; the size and shape of the table that the ball is on, the coefficient of friction between the ball and table is zero, the collisions between the ball and the wall is completely elastic, the initial velocity of the ball is greater than 0, and the $\alpha $ of the stadium table is greater than or equal to zero.

## Outline
- The first objective to be complete is to obtain the plots and results given in Giordano's book for the phase-space plot and the divergence plot. Once these are obtained we will then test how changing the length of the stadium table and initial conditions of the ball effect its trajectory. 

Once data has been collected for the different stadium tables, we will then create functions for different tables that allows us to move between table shape and size. We will then test the ball's trajectory and how it is effected by the different table shapes and size. For each specific table, multiple tests will also be ran for different initial conditions.

- The outputs that are expected consist of two main plots. For every table we will output phase-space plots to help understand the trajectory of the ball as it is effected by different tables. We expect to have multiple plots for different initial conditions of each table as well. The next plot expected is the divergence plots of the trajectory. With this we will be able to observe how the Lyapunov exponent is changed by different lengths for the sides of stadium tables, along with different shaped tables.

- Results can be checked for correctness by comparing them to results found by others who have written papers on similar project. These can be found online or in other articles.

## Timeline
- Have simulations and models similar to the ones givens by Giordano that run accurately - 4/25/2018

- Have the first question and set of test completed for different stadium tables and initial conditions - 4/27/2018

- Complete model for elliptical table, and if the elliptical table is completed early a square table. Have the plots and analysis completed  for the trajectory of both the different billiards and these tables completes. - 5/2/2018

-Have final models complete, along with analysis and results. - 5/5/2018

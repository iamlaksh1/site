---
title: "Engineering Mechanics - Statics "
date: "2025-11-29" 
tags:
  - "gis"
  - "Engineering Mechanics"
  - "Physics"
  - "Free body diagram"
  - "Forces"
  - "Equilibrium"
  - "Trignometry"
  - "Statics"
---

Recently, I’ve been revisiting some basic statics problems, especially those involving force resolution. In this post, I will walk through types of forces, and how to construct free body diagram and solve the equations with some of key principles and guidance with figures. I also provided classic example of understanding Newtons Laws of Motion with an example. 


<h4> Types of Forces</h4>

 Here are some of the fundamental forces you’ll encounter while constructing free-body diagrams:

- Gravitational Force:
The weight of an object, always acting vertically downward toward the center of the Earth.

- Normal Force:
The support force exerted by a surface. It always acts perpendicular to the surface and counterbalances the tendency of an object to “press into” that surface due to gravity.

- Frictional Force:
A resistive force that acts opposite the direction of motion (or attempted motion) when one surface slides or tends to slide over another.

- Tension Force:
A pulling force transmitted through a rope, cable, or string. It acts along the length of the rope and pulls equally on the objects it connects.

<div style="display: flex; gap: 10px; flex-wrap: wrap; margin-bottom: 20px;">
  <img src="../images/normal_force.png" alt="Normal Force" style="width: 300px; height: auto;">
  <img src="../images/normal_force_1.png" alt="Normal Force" style="width: 300px; height: auto;">
  <img src="../images/frictional_force.png" alt="Frictional Force" style="width: 300px; height: auto;">
</div>



<h4> How to construct Free Body  Diagram </h4>

1. Isolate the particle/object - The term "free-body" refers to seperating the object or particle from its support. Ignore all extra /physical connections to the object. 

Example of Free body digram for Box A :

  ![FBD of Box A](../images/fbd-box.png)
  ![FBD of Box Pulley](../images/fbd-pulley.png)
      ![Forces on small weight ](../images/small-weight.png)
      ![Forces on large weight ](../images/large-weight.png)

2. Set up a coordinate system –This super important how to set-up a coordinate system. Does the coordimnate system (x-y plane) parallel to line of action or surface? Or clockwise direction as  positive or anti-clockwise direction as negative direction of forces? 

      ![Coordinate Systen](../images/coordinate-system.png)

3. Identify all applied loads – Show all forces acting on the body, including pushes, pulls, and the body’s weight if it’s significant. Each force should have a variable name and a clearly drawn arrow indicating its direction. 

    - *Take only the External forces acting on the mass*

    - *Take only External forces applied*

    - *Inter-molecular forces vibration molecules /moving electrons should be  ignored. Since their vector sum is zero. Just think, if   vector is not zero then the object will not be stationary*. (see image below)

    - *Forces the mass is impression on other masses this should be ignored*.

      ![Internal Force](../images/internal-force.png)
  


4. Determine support reactions – These forces come from the supports you removed when isolating the body. Particle supports act as two-force members, producing either tension or compression.

5. Label everything clearly – Make sure every force on your diagram has either a numerical value or a symbolic variable if the exact value is unknown. The completed free-body diagram should be neat, fully labeled, and ready for analysis.



<h4> Few Points </h4>

1. Does magntidue to force is negative then vector is opposite direction 

2. Tension on any string /cable/ pulley are Tensile force 

3. Frictionless pulley or rope is massles or rope is inline with mass center 

4. System is  in Equilibrium.  $\sum F_x = 0$ and $\sum F_y = 0$

5. Weigh is equal to $W = Mg$ 

 <h4> Solving Equilibrium Equations </h4>

  1. Break vectors into components. Compute each force’s x and y components
  using right-triangle trigonometry.

  2. Write equilibrium equations. Now represent your free-body diagram as two
  equilibrium equations, ΣFx = 0 and ΣFy = 0.
  3. Count knowns and unknowns. At this point, you should have at most two
  unknown values. If you have more than two, reread the problem and look
  for overlooked information.
  4. Solve for unknowns. Use algebra to simplify the equilibrium equations
  and solve for unknowns. All answers in Statics will have units - unless you
  have solved for a dimensionless value, like a friction coefficient. 
  5. Check your work. If you add the components of the forces, do they add
  to zero?  Do the results seem reasonable given the situation? Have you
included appropriate units?

<h4> Example to understand Newtons Law of Motions  </h4>

![Action and Reaction DO NOT CANCEL OUT](../images/force-man.png)

When a person pulls a block with a rope. The block pulls back with the same force. But the block moves while the person stays put. Why?

The key is understanding the difference between Newton’s Second and Third Laws. The Second Law looks at the forces on a single object to determine its motion. The Third Law talks about the interaction between two objects. The Third Law itself doesn’t tell you whether an object will move—it’s the net force on each object that matters.

In the block example, the block slides because the person’s pull is stronger than friction. But the person stays in place because their shoes prevent slipping, and friction balances the pull of the rope. The net force on the person is zero, so they don’t move.

In short, action and reaction forces don't cancel because they act on different objects. Each object's motion depends on the net force on it, according to Newton's Second Law. 

*Note 1: Newton Second Law - Only forces acting on a given body - here an box - where two forces involved - Pull force by man, and Frictional force. Sum of these forces determies acceleration*.

*Note 2: Newton third Law - Relates the forces on two different bodies exert on each other ; this does not tells nothing about motion of either body* 


![Action and Reaction DO NOT CANCEL OUT](../images/newton-laws.png)


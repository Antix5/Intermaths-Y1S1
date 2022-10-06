## Modeling of Continuous Mediums

### Introduction

In this section, we will discuss the modeling of continuous mediums. We will start with the simplest case and complexify the equation step by step

<div class="container">
  <div class="cube">
    <div class="face top"></div>
    <div class="face bottom"></div>
    <div class="face left"></div>
    <div class="face right"></div>
    <div class="face front"></div>
    <div class="face back"></div>
  </div>

  <div id="At"> A(t) </div>
</div>

<style>

.container {
  width: 200px;
  height: 200px;
  perspective: 500px;
  margin: 50px;
}

.cube {
  position: relative;
  width: 200px;
  height: 200px;
  transform-style: preserve-3d;
}

.face {
  position: absolute;
  width: 100px;
  height: 100px;
  border: 2px solid black;
}

.front {
  transform: translate(50px, 50px);
}

.left {
  transform: skew(0deg, 45deg) translate(0px, 25px);
  width: 47px;
}

.right {
  transform: skew(0deg, 45deg) translate(102px, -78px);
  width: 47px;
}

#At {
  position: absolute;
  transform: rotateY(25deg) translate(70px, -125px);

}

</style>

Let consider a region $A(t)$ in 3D space. This region of space can be consider as an element of the continuous medium we are modeling.

We can firstly work on the kinetic of the continuous medium. We are in the setting of classical mechanics, so we can use the Newton's law of motion.

The Newton's law of motion is the following:

$$\sum_{i=1}^n \vec{F}_i = \frac{d\vec{p}}{dt}$$

where $\vec{F}_i$ are the forces acting on the element, $\vec{p}$ is the momentum of the element and $t$ is the time.

We can firstly transform this equation to adapt it to the continuous medium.

$\vec{p} = \int_{A(t)} \rho \vec{v}  d\sigma$

where $\rho$ is the density of the medium and $\vec{v}$ is the velocity of the medium.

We can now take into account the forces acting on the medium. There are two types of forces acting on the medium:

*   The forces acting on the medium due to the interaction with the environment

... to be continued
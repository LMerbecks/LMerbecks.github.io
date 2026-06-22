---
title: "Radio Controlled Flying Rectangle"
excerpt: "Radio controlled airplanes offer a great playground for experimenting with mechanical and electrical design concepts. While the only limit is ones imagination RC airplanes need not be scaled model versions of real airplanes. They can be as simple as a wing with a propeller and control surfaces. To built such a simple plane is the goal of this project.<br/><img src='/images/flying-rectangle/flying-rectangle-in-the-field_cropped.jpeg'>"
collection: portfolio
author_profile: false
---

{% include toc %}

**Radio controlled airplanes offer a great playground for experimenting with mechanical and electrical design concepts. While the only limit is ones imagination RC airplanes need not be scaled model versions of real airplanes. They can be as simple as a wing with a propeller and control surfaces. To built such a simple plane is the goal of this project.**

![RC flying rectangle in the field](/images/flying-rectangle/flying-rectangle-in-the-field_cropped.jpeg)
*The RC airplane developed in this project out in the open field after a test flight.*

> „Making something that can fly isn’t that complicated. By following a few simple rules you can get this sheet of foam to fly in like half an hour“ 
> ~ Samm Sheperd, 2016

# Introduction
RC planes are a great way to get into electronics and mechanical engineering. The combination of knowledge in both disciplines is what makes these vehicle fly. Many RC aircraft are scaled versions of real aircraft. However, one of the benefits of RC planes is that you are not limited to this kind of aircraft. I got inspired to build one of the most simple RC planes via [this video](https://youtu.be/Y2pwgJU5bfM?is=rDv9w5LtFTxpw5mM) of [Samm Sheperd](https://youtube.com/@sammsheperd?si=tJuPN8SVNwCpClft) . In the video he builds a flying wing based on a piece of foam board and only a handful more parts. 

# Methods 
The engineering methods applied in this project can be split into design and manufacturing. These two topics are addressed in individual sections.

## Design

To design the flying rectangle principles shown in the video of Samm Sheperd are applied. Where appropriate they are adjusted or amended with additional principles. 

The airplane is an elevon controlled flying wing with constant chord and no sweep. The main building material is foam board. Propulsion and control actuation is performed electrically and control signals are transmitted via an analog RC transmitter, receiver pair from FlySky. 

An important factor for flight stability of this airplane (and airplanes in general) is the position of the center of gravity. To determine this for the given geometry [this online tool](https://fwcg.3dzone.dk/ext/Flying%20Wing%20CG%20Calculator%20V3.html) is used. In addition to the wing geometry it also allows to add other components with mass and COG position. Using this functionality all other components, such as ESC, motor, battery etc. are added. Then a placement for these components is found that puts the center of gravity in the right position for stability. As a challenge to myself I also developed a center of gravity calculator using python. The resulting layout form the website is shown in the figure below.

![Layout of components for the flying wing](/images/flying-rectangle/cog_calculator_layout.png)
*Component placement for the flying rectangle. Red: Motor, Blue: Servos, Yellow: ESC, Black: RC receiver, Cyan: Battery*

To ensure yaw stability the flying rectangle gets a vertical stabilizer. This gives the aircraft weather vane stability. 

Additionally, to the layout a motor mount and servo control horns are designed and manufactured with a FDM printer. The motor mount went through two iterations. The first iteration is a simple right angle bracket with some support. It became apparent during manufacturing that the motor and the battery had to be offset from the leading edge forward to achieve an acceptable center of gravity position. Thus a second version of the motor mount moved the motor beyond the leading edge and also included a spot for the battery to be mounted with a velcro strap. The following figure shows the CAD models of the two motor mounts.

![Geometry of motor mount 1](/images/flying-rectangle/simple-motor-mount.png)
*Version 1 of the motor mount for the flying rectangle.*
![Geometry of motor mount 2](/images/flying-rectangle/truss-motor-mount.png)
*Version 2 of the motor mount for the flying rectangle.*


The servo control horns are a simple geometry that allows the push rods to be mounted at the same hinge radii as found on the actual servos. A flap is added to the geometry for additional glueing surface and to serve as a stop when inserting the control horn into the control surface. The geometry is shown in the figure below.

![Servo control horn geometry](/images/flying-rectangle/servo-horn.png)
*Geometry of the FDM-printed control horn*

## Manufacturing

The base material for this airplane are three DIN A3 foam boards. Two of these are hot-glued together on the long edge to form a DIN A2 sized sheet of foam. This sheet is the wing and simultaneously the structure in this build. To make it more resilient against water the sheet is covered with packaging tape. This is a technique I learned from Samm and widely used in the RC plane community. 

After the basic structure is done large elevons are cut from the sheet as control surfaces. The control surfaces are chamfered and hinged to the structure with packaging tape. Next the servo control horns are hot-glued in place. After this the push rods for the servos can be manufactured from music wire and the servos are then glued onto the wing.

The motor is installed on the designed motor mount which is then hot-glued in place on the leading edge of the wing. After test flights structural ribs are added on the top and the bottom side of the wing to distribute the bending loads during crashes into the airframe better. Before the motor mount was not rigid and the foam structure risked failure around it due to overstressing. The motor is equipped with a prop saver which prevents propellers snapping if they are not parallel to the wings leading edge during landing.

The vertical stabilizer first was the same length as the elevons. It became apparent quickly that this generated a weak point in the airframe between the elevons. Thus, the vertical stabilizer is increased and bending stiffness of the airframe is greatly increased around the y axis. The first airframe version still using the shorter vertical stabilizer is shown in the figure below.

![First airframe version](/images/flying-rectangle/first-version-rectangle.jpeg)
*First version of airframe with slim vertical stabilizer and no structural ribs.*

All other components where glued down at the locations specified in the design phase. The battery is secured on the plane with a velcro strap. In the end the center of gravity position is double checked. The final result of the airframe is shown in the following figure.

![Picture of finished airframe](/images/flying-rectangle/rigid-version-rectangle.jpeg)
*Finished airframe of the flying rectangle.*

# Result

The result of this project is a very simple RC plane that is easy to manufacture. The flying qualities are acceptable. Overall the aircraft is stable but the roll authority is slightly too large for the mass distribution concentrated on the centerline. This can be fixed by adjusting the aileron weights in the signal mixing for the elevon control signals on the RC transmitter. During multiple pilot induced crashes the airframe was slightly damaged. Importantly, however, these damages are easy to fix due to the simplicity of the airframe and thus interrupted flight operations only momentarily. The very first flight tests also uncovered the problems discussed previously in the Design section such as the weak point around the vertical stabilizer and the lack of rigidity in the motor mount. Another benefit of the resulting low cost airframe is that it produces ease of mind for the pilot as crashes only cause minimal harm to the airframe. The flying rectangle has sufficient power to be launched by hand and thus does not need landing gear. The following picture shows the airplane out in the field.

![Flying rectangle in the field](/images/flying-rectangle/flying-rectangle-in-the-field_cropped.jpeg)
*The flying rectangle during flight test.*

# Conclusion & Outlook

Overall the goal of building a cheap plane was accomplished. During the project I learned a lot on mechanical design, manufacturing techniques and electronics. The resulting plane is considered an adequate flying wing trainer because of the good stability and the ease of launching. The most significant problem of this plane is that there are huge loads on the propeller when it is not parallel to the leading edge during landing. 

This project also sparked my interest in [flow5](https://flow5.tech/flow5.html), an open-source software to analyze low Reynolds number flows and airplane geometries. In the future I want to try to analyze the airframe geometry of the flying rectangle for its eigenmodes, stability and more. Moreover, the project inspired me to look at digital RC transmitters and receivers, and the possibility to install a flight controller on the aircraft. With a flight controller the flight characteristics of the airplane could be further tuned through roll/pitch damping or advanced control laws. 

# In Memoriam
This article is dedicated to Samm Shepperd who sadly passed away in 2018. For me personally he was the inspiration to start with RC airplanes and contributed to me becoming a mechanical engineer.
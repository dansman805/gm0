# Holonomic Drivetrains

## Mecanum Drive

Mecanum drivetrains consist of four mecanum wheels which are powered independently by one motor. This configuration angles the velocity of each wheel, allowing the robot to strafe.

The primary advantage to mecanum drive is the maneuverability it affords, especially because the robot can strafe instead of turn and drive. The rollers on mecanum wheels form a 45 degree angle with the wheel’s axis of rotation, which means that mecanum drivetrains can’t strafe as fast as they can drive forward.

This can be explained by discussing the forces involved. When each wheel rotates, it applies a friction force to the ground, which moves the robot. When moving forward, both sets of left wheels rotate in the same direction at the same speed, and both sets of right wheels rotate in the same direction at the same speed, meaning that the forces do not oppose each other. However, when strafing, neither the two left wheels nor the two right wheels are rotating at the same speed. In many cases, they even rotate in opposite directions.

These two opposing forces cause the rollers to slip more and more, which angles the robot’s velocity at the expense of traction (more slipping results in a loss of speed). However, the wheels do still slip when moving forward but not as drastically as they do when strafing.

This is the primary disadvantage to mecanum drivetrains: they tend not to have much pushing power and thus, are vulnerable to defense by a sturdy tank drive.

Due to the fact that mecanum wheels are more likely to slip because of the diagonal rollers, an optional addition to mecanum drives is a separate odometry mechanism in order to track the robot’s location during autonomous.

:::{attention}
It is important to note that in order to maximize the efficiency and stability of mecanum drives, when viewed from above, the rollers of each wheel should point towards the center of the robot, forming an X shape, rather than a rhombus.

The primary reason for this is that it allows the drivetrain to turn significantly faster than it would otherwise be able to. When using the suggested setup, when viewed from the robot’s underside, the rollers form a rhombus. This allows the force applied by the wheels on the ground to act tangent to the turn radius, leading to faster turning.
:::

### Advantages

- Fantastic maneuverability and agility due to strafing, can avoid defense very well
- Good acceleration, can have high top speed
- Very versatile drivetrain for nearly any game

### Disadvantages

- Suffers in traction, as mecanum rollers have a lower coefficient of friction than traction wheels; cannot traverse terrain
- Able to be pushed around on defense
- Wheels must be powered independently, so there is no redundancy

:::{figure-md}
:width: 100%
![Diagram of mecanum directions](images/holonomic/gobilda-mecanum-direction.png)

Configuration for mecanum wheels, courtesy goBILDA
:::

### Mecanum Wheels Miniguide

There are plenty of mecanum wheels on the market, and it can be very daunting to choose between the many vendors. An important feature is the type of mechanism that facilitates the motion, either {term}`bushing <Bushing>` or {term}`bearing <Ball Bearing>`. Bearing based mecanum wheels often have superior strafing because there is less resistance for the rollers to overcome. Another important note is that some FTC teams invest in 6 inch mecanum wheels instead of 3 or 4 inch mecanum wheels, often at a much higher price. **It is highly recommended that teams stick with 3 or 4 inch mecanum wheels**. Here is a general list of the mecanum options ranked in order of recommendation.

1. [goBILDA Mecanum Wheels][gobilda mecanum wheels] ($105 with team discount): This recent addition to the lineup has become one of the strongest options for its variety of positive attributes. goBILDA Mecanum wheels are based on the tried and tested Nexus bearing mecanum wheels, which means it has fantastic strafing.

   They are also very robustly built, and are significantly more convenient to mount to FTC standard build systems. Thy have a built in goBILDA 16mm and 32mm hole pattern, and has easy support for dead axle.

   You can mount hubs in wheels and goBILDA mecanum wheels can easily mount to 1/2" Hex, 3/8" Hex, 12 mm REX, 6 mm D, 1/4" D, and many other shafts. Hubs can also be mounted inside the wheel for very low profile mounting. It is also the cheapest bearing mecanum on the market.

   Due to its convenient mounting and fantastic strafing performance, we recommend all teams consider goBILDA mecanum wheels.

   :::{note}
   These are tied with the [REV 75mm Mecanum Wheels][rev 75mm mecanum wheels] ($76.50 with team discount): These mecanums are uniquely positioned due to their compact size, at just 75mm (~3 inches) in diameter and 40mm wide. They can be easily mounted to 5mm hex shaft with an included adapter. They are also bearing based, which give them great strafing performance.
   :::
2. [Nexus Bearing Mecanum Wheel][nexus bearing mecanum wheel] ($134): This was the old gold standard, and still has fantastic performance for the price.

   This has identical performance with goBILDA mecanum wheels, however is slightly less convenient to mount to. However, these wheels feature the 1.875" bolt pattern commonly used in FRC{{ reg }} motion products.

   It is also slightly heavier than goBILDA Mecanum wheels. Many teams will 3D print adapters or build new cores for Nexus Mecanum wheels. Even though the goBILDA mecanum offer advantages and very few disadvantages over Nexus bearing wheels, these wheels remain a solid option.
3. [AndyMark Heavy Duty 4” Mecanum Wheel][andymark heavy duty 4” mecanum wheel] ($225): These are easily the most expensive mecanum wheels on the list. These are bushing based mecanum, so they have decent strafing, albeit not as good as the goBILDA and the Nexus bearing mecanum wheels.

   What sets these mecanum wheels apart is the 80A roller material. AndyMark HD mecanum wheels have higher traction than all other mecanum wheels, which make them desirable for climbing terrain. For example, during the Relic Recovery season, teams had to climb a “balancing stone”, and many teams chose to use the AndyMark HD mecanum wheels to be easily able to climb the balancing stone.

   However, in most cases, being able to more effectively strafe is more important than having good traction. For this reason, **teams are recommended to buy bearing based mecanum wheels like the REV, goBILDA, or Nexus mecanum wheels instead of the AndyMark HD wheels due to the major price difference**.
4. [Nexus Bushing Mecanum Wheel][nexus bushing mecanum wheel] ($84): This is the Nexus Bearing Mecanum wheel with bushings instead of bearings. Before the introduction of the goBILDA mecanum wheels, these were the best budget option, however, it is now more sensible to spend the $21 premium to get the bearing goBILDA mecanum wheels.
5. [VexPro Mecanum Wheels][vexpro mecanum wheels] ($119.96): These mecanum wheels are most suited for vectored intakes on FRC{{ reg }} robots. They are relatively tough, but have somewhat poor strafing and are not quite as durable as the other wheels higher on the list. They are a decent choice if you already have them, but otherwise, there is no reason to consider them.
6. [TETRIX Mecanum Wheels][tetrix mecanum wheels] ($113): At the time of writing this guide, these haven’t been released so no verdict can be reached. However, they have a built in hub so they can be easily mounted on 6mm D shaft. They are bushing based, and due to no testing and evaluation outside of TETRIX, and its higher price than the goBILDA mecanum wheels, **we cannot recommend the TETRIX Mecanum Wheels**.
7. [VEX EDR Mecanum Wheels][vex edr mecanum wheels] ($59.99): These are the cheapest mecanum wheels, but have a strange shaft standard (1/8" square) which require the use of 3D printed adapters. **There are not many reasons to purchase these wheels.**
8. [AndyMark Standard Duty Mecanum Wheels][andymark standard duty mecanum wheels] ($92): **DO NOT PURCHASE THESE WHEELS**. These are terrible mecanum wheels. They barely strafe and are super fragile. Just buy goBILDA mecanum wheels for $13 more.

[gobilda mecanum wheels]: https://www.gobilda.com/96mm-mecanum-wheel-set-70a-durometer-bearing-supported-rollers/

[nexus bearing mecanum wheel]: https://www.superdroidrobots.com/shop/item.aspx/4-inch-nexus-mecanum-wheels-ball-bearing-set-of-4/1352/

[andymark heavy duty 4” mecanum wheel]: https://www.andymark.com/products/4-in-hd-mecanum-wheel-set-options

[nexus bushing mecanum wheel]: https://www.amazon.com/100Mm-Aluminum-Mecanum-Wheel-Right/dp/B01CTUT4GY

[vexpro mecanum wheels]: https://www.vexrobotics.com/mecanum-wheels.html

[tetrix mecanum wheels]: https://www.pitsco.com/TETRIX-MAX-Mecanum-Wheels

[vex edr mecanum wheels]: https://www.vexrobotics.com/edr-wheels.html

[andymark standard duty mecanum wheels]: https://www.andymark.com/products/4-in-standard-mecanum-single-wheel?via=Z2lkOi8vYW5keW1hcmsvV29ya2FyZWE6OkNhdGFsb2

[rev 75mm mecanum wheels]: https://www.revrobotics.com/rev-45-1655/

:::{figure-md} 
![8103 Null Robotics's mecanum drivetrain render](images/holonomic/8103-mecanum.png)

8103 Null Robotics, Rover Ruckus, **using Nexus bearing mecanum**
:::

:::{figure-md} 
![9829 MakBots's mecanum drivetrain](images/holonomic/9829-mecanum.png)

9829 MakBots, Relic Recovery, using **VexPro mecanum**
:::

:::{figure-md} 
![731 Wannabee Strange's mecanum drivetrain render](images/holonomic/731-mecanum.png)

731 Wannabee Strange, Rover Ruckus, using **AndyMark HD mecanum wheels**
:::

## X-Drive

X-Drive is a holonomic omni-wheel based drivetrain. This type of drive involves mounting 4 omni wheels at the corner of the robot at a 45 degree angle.

One notable difference between X-Drive and mecanum is strafe speed. While, as mentioned in the mecanum section, the ratio of strafe speed to forward speed is noticeably less than 1, the ratio on an X-Drive is exactly 1 due to the rotational symmetry of the wheel placement. This means that an X-Drive bot’s strafe speed and forward speed are equivalent. The drivetrains are slower, however, when strafing at 45° (approximately {math}`\frac{\sqrt{2}}{2}` of its forward speed).

Even though X-drive has good turning and acceleration, the main downside to the drive is packaging/form factor. Packaging refers to how easy/convenient the drivetrain fits into the overall design of the robot.

Ideally, the drivetrain should take up as little space as possible to make it easier to design mechanisms around. Because the omni wheels are offset, packaging a X-Drive is more difficult than other types of holonomic drive like mecanum or H-Drive. Also because of the strange packaging, it is relatively difficult to cleanly transfer power from the motors to wheels, meaning that most X-Drives end up being direct-driven, which is bad for the lifespan of the motor gearbox.

:::{note}
When using X-Drive, the robot moves forwards/backwards/straight side-to-side {math}`\sqrt{2}` times faster than a drivetrain with wheels in the normal orientation (with the same gear ratio and wheel size).

For an explanation of why exactly this is, see [this analysis](<https://www.chiefdelphi.com/t/paper-mecanum-and-omni-kinematic-and-force-analysis/106153>).
:::

### Advantages

- Good maneuverability and agility
- Good acceleration

### Disadvantages

- Prone to defense, pushed around easily
- Often uses direct drive due to awkward form factor

:::{figure-md} 
![731 Wannabee Strange's X-Drive](images/holonomic/731-xdrive.png)

731 Wannabee Strange, Velocity Vortex
:::

:::{figure-md} 
![5040 Nuts and Bolts's X-Drive](images/holonomic/5040-xdrive.png)

5040 Nuts and Bolts, Relic Recovery
:::

## H-Drive

H-Drive (also known as U-drive, depending on the configuration) is a holonomic type drive that uses all omni wheels. H-Drive relies on a set of “strafer wheels” that are perpendicular to the forward/backward wheels to achieve strafing. H-Drive is similar to a fusion of a tank drivetrain while retaining the maneuverability and strafing of holonomic drivetrains.

H-Drive is theoretically very easy to code, but most teams employ some sort of gyro correction to strafe straight, although it is not necessary with proper weight distribution.

H-Drive has a number of possible motor configurations - 1 or 2 motors can be put on each forward drive pod, and one or two motors can be put on the strafe wheels. In the configuration with one motor on each forward drive pod, H-Drive has slightly reduced acceleration compared to mecanum drive.

For the highest possible reliability, many FRC{{ reg }} teams will suspend their strafe wheels on a rocker system to ensure that all wheels are in contact with the ground while the robot is not strafing.

By far the biggest advantage of H-drive is its ability to accommodate multiple motor distributions. For instance, if you want to dedicate only 3 motors to your mechanisms and you have a motor left over, using a 1 strafe motor, 4 drive motor configuration is absolutely viable. Or if you dedicate 5 motors for your mechanisms, H-drive with 2 drive motors and 1 strafe motor is definitely optimal.

### Advantages

- Combines tank and holonomic drivetrain advantages
- Can be used with 3 or 5 motors
- Good traction and top speed
- Great maneuverability and agility

### Disadvantages

- Strafing is slightly less effective than mecanum
- Complex suspension occasionally needed, depending on design

:::{figure-md} 
![9804 Bomb Squad's H-Drive](images/holonomic/9804-hdrive.jpg)
:::


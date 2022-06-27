# Introduction

[Official WPILib Documentation](https://docs.wpilib.org/en/stable/docs/software/kinematics-and-odometry/swerve-drive-kinematics.html)

For extra info [Team 1640's Swerve](https://team1640.com/wiki/index.php/Swerve_Central)

**Swerve drive** is a system alternative to West Coast Drive in which two joysticks are used: one to control moving horizontally and vertically, and one for rotation. This has numerous advantages:

- MUCH easier to build
- More intuitive to drive:
    -Instead of having to think from the robot’s perspective, swerve drive allows the driver to think from their own perspective. In other words, swerve drive is **field-oriented**.
    -Swerve drive allows two people, one piloting with the other shooting/picking up cargo/etc., to drive at the same time more efficiently.

To code swerve drive, we use 2D vectors. A **vector** represents a direction and magnitude in the X-Y plane. We denote vectors by a point on the plane (x, y). The vector is the path on the plane from the origin to (x, y). In swerve drive, each of the four wheels on the robot has a position vector.

Swerve drive also utilizes information from encoders. **Encoders** are devices that record the number of revolutions or “ticks” of an axle or gear. They can be external or internally built-in, as in a Spark-MAX. 

Encoders function through induced magnetic flux. This means that when an encoder starts or stops turning, it produces a voltage (positive or negative based on the direction the gear is rotating). This voltage corresponds to a digital input of 1 or true. When an encoder is not changing (it either remains still or in motion), no voltage is produced. This corresponds to a digital input of 0 or true. 
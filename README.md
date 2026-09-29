# Modular Autonomous Mobile Robot (AMR) for Smart Warehouse Automation

**Smart India Hackathon 2026 · Team_7 · SiH-26112**

**Problem Statement:** Design and Develop a Modular Autonomous Mobile Robot (AMR) Platform for Smart Warehouse Automation
**Theme:** Robotics and Drones · **Category:** Hardware · **Team ID:** 158819

## The problem
- Conventional AMRs transport items only at floor level.
- Multi-level racks need a mechanism to reach elevated storage locations.
- Fixed AS/RS solutions are tied to dedicated rack and aisle infrastructure.
- Different rack heights require flexible vertical positioning during retrieval.
- Existing warehouses need solutions that integrate without major rack modification.

## Our solution
An autonomous robot that combines mobility, a lifting platform and a telescopic reach into one unit for rack-level item retrieval, designed to fit existing warehouse racks with minimal modification.

**Key innovation**
- Mobile + lift + telescopic reach in one robot
- Automated rack-level access across different heights
- Adaptive gripping for varied item/box sizes
- Minimal rack modification for deployment
- Modular mechanical architecture for scalable development

**How it works**
1. The autonomous robot navigates to the rack for item retrieval.
2. The rising platform reaches the required rack level.
3. The telescopic arm extends into the rack.
4. The adjustable gripper accommodates different box sizes.

## Technical approach
**Hardware:** AMR chassis, telescopic arm, adjustable rubber-padded gripper, Raspberry Pi 5 controller, motor drivers, LiDAR/depth sensing, camera, proximity/safety sensors, IMU and wheel encoders, battery system

**Software:** ROS 2, Nav2, SLAM, MoveIt 2, Rviz2, Gazebo, Autodesk Fusion, Codesys

**System workflow**
1. Sensing → Localization → Navigation → Rack alignment
2. Platform lift
3. Telescopic extension → Gripping
4. Retraction → Transport & placement

## Feasibility, risks and mitigation
| Aspect | Feasibility | Key risk | Mitigation |
|---|---|---|---|
| Navigation & localization | ROS 2 + LiDAR navigation is well established | Dynamic obstacles, localization error | Sensor fusion + obstacle detection |
| Rack alignment | Depth/proximity sensing supports alignment | Lateral offset at the rack | Closed-loop fine alignment before lift |
| Lifting mechanism | Actuated linear lifting is readily implementable | Load variation, mechanical deflection | Payload limits + structural analysis + position feedback |
| Telescopic arm & gripper | Controlled linear reach with adjustable grip | Cantilever load, varied item sizes | Payload limits + support/locking + grip range limits |
| Stability & payload | Low-mounted battery supports stability | CG shift during arm extension | Wide base + low CG + extension limits |
| Safety | Sensors can support safe operation | Collision with people or racks | Obstacle sensing + speed limits + emergency stop |
| Manufacturing & maintenance | Modular design with standard components | Wear in moving parts, alignment drift | Modular parts + periodic calibration |

## Impact and benefits
- **Warehouse operations:** automated multi-level retrieval; less repetitive manual handling
- **Productivity:** continuous material movement; consistent retrieval workflow
- **Safety:** less manual heavy handling; controlled robotic retrieval
- **Infrastructure:** built for existing racks; minimal rack modification
- **Scalability:** modular mechanical design; adapts to warehouse layouts
- **Economic potential:** potentially less manual handling; reusable multi-task platform

## Repository structure
| Path | Contents |
|---|---|
| [`PPT/`](PPT) | Idea submission presentation (PDF and PPTX) |
| [`Design-Autodesk Fusion/`](Design-Autodesk%20Fusion) | CAD design, stress/optimization results and videos |
| [`AMR_assembly design.step`](AMR_assembly%20design.step) | Assembly model (STEP format) |

**Assembly file:** https://a360.co/3Vkj5lU

## References
- Macenski et al., "Robot Operating System 2: Design, Architecture, and Uses in the Wild," *Science Robotics*, 2022. https://doi.org/10.1126/scirobotics.abm6074
- Loganathan & Ahmad, "A Systematic Review on Recent Advances in Autonomous Mobile Robot Navigation," *Engineering Science and Technology*, 2023. https://www.sciencedirect.com/science/article/pii/S2215098623000204
- "Mechatronic System Design of a Smart Mobile Warehouse Robot for Automated Storage/Retrieval Systems," IEEE ASYU, 2020. https://doi.org/10.1109/ASYU50717.2020.9259882
- Roodbergen & Vis, "A Survey of Literature on Automated Storage and Retrieval Systems," *European Journal of Operational Research*, 2009. https://www.sciencedirect.com/science/article/pii/S0377221708001598
- Macenski et al., "The Marathon 2: A Navigation System," IROS, 2020. https://doi.org/10.1109/IROS45743.2020.9341207

## Team
Team_7 – Smart India Hackathon 2026

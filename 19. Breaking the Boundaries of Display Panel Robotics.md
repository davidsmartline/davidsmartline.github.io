


# Breaking the Boundaries of Display Panel Robotics: Technical Insights from Visiting a Leading Flat Panel Display Factory

During a recent industry exhibition, our technical team had an in-depth exchange with the engineering division of a major flat panel display manufacturer regarding the application of our **novel non-linear scissor-arm technology** in robotic physical structures. Following their kind invitation, we conducted an on-site technical inspection and discussion at their cleanroom production facility.


This article documents that visit the technical parameters of current industry standards, and our innovative architectural solutions for next-generation display manufacturing robots.


### 1. On-Site Inspection of the FPD Cleanroom Production Line

The flat panel display factory maintains exceptionally strict confidentiality protocols. Before entering, we were required to sign non-disclosure agreements, seal our mobile phone and computer camera lenses, and don specialized cleanroom garments, hoods, and booties.


The production line is laid out in a **U-shape**:


- Raw glass substrates are retrieved one by one from the glass storage racks at the entry point by massive dual-Scara arm robots and placed into processing chambers.


- After processing, identical dual-arm robots extract the substrates from the other end and transfer them into the next processing chamber.


- This cycle continues through various manufacturing stages until the finished glass returns to the exit-end storage racks.


The line employs approximately six nearly identical dual-Scara arm robots, utilizing units manufactured by Korea's **Hondai**.


### 2. Core Technical Parameters Provided by the Client

The client outlined the specifications for developing an 8G-class robot platform:


- **Rotation Radius:** The circumferential or cylindrical space required for base rotation when the arm is fully retracted at the origin: $\\le 2000\\,\\text\{mm\}$.


- **Stroke / Extension Range:** Passline height ranges from $1300\\text\{--\}6000\\,\\text\{mm\}$ (customizable based on requirements). Arm extension reaches $4800\\,\\text\{mm\}$.


- **Base Rotation:** $360^\\circ$.


- **Travel (Linear Track):** Customized based on the factory layout, typically up to $\\sim 16\\,\\text\{meters\}$ (travelling on an integrated rail).


- **Arm Configuration:** Dual arms capable of **Exchange actions**—one arm retracts with a substrate while the other simultaneously extends to place a substrate.


- **Cleanroom Class:** Class 10.


- **Repeatability:** $\\pm 0.25\\,\\text\{mm\}$ (long-term guaranteed).


- **End-Effector Stability:** Low vibration at the arms, particularly at the fork tips.


- **Arm Pitch (Inter-arm spacing):** $92\\text\{--\}160\\,\\text\{mm\}$.


- **Glass Dimensions & Weight:**


  - Substrate sizes vary across generations: Gen 6 ($1500 \\times 1800\\,\\text\{mm\}$), Gen 8.5 ($2500 \\times 2200\\,\\text\{mm\}$), Gen 8.6 ($2290 \\times 2620\\,\\text\{mm\}$), Gen 10 ($3370 \\times 2940\\,\\text\{mm\}$). (A clear trend toward larger substrates).


  - For the target 8.6G line: Glass dimensions are $2290 \\times 2620 \\times 0.4\\,\\text\{mm\}$. Weight is $6\\,\\text\{kg\}$ per single sheet, and $15\\,\\text\{kg\}$ for bonded double sheets.


#### Key Q&A Insights:

1. **Extension Distance:** While the total reach is referred to horizontally, the actual active extension currently reaches $4600\\,\\text\{mm\}$.


2. **Repeatability:** The $\\pm 0.25\\,\\text\{mm\}$ repeatability applies to both longitudinal (front/back) and lateral (left/right) directions.


3. **Positioning Methods:** Photolithography process steps on the line utilize **vision positioning**, while other steps rely on mechanical 4-corner, 8-point alignment mechanisms to push and register panels.


4. **Industry Benchmarks:** When asked which manufacturers supply robots for industry giants like Samsung and Sanyo, they noted that these companies predominantly **produce and use their own proprietary robots**.


### 3. Key Technical Challenges Raised by the Client

1. **Sag and Vibration Limits:**


   - **Requirement:** Vertical jitter, oscillation, or sag of the glass substrate when extending into or retracting out of glass racks or process slots **must not exceed approximately $25\\,\\text\{mm\}$**.


   - **Challenge:** They requested a simulated sag-variation curve for arm extension prior to physical prototyping.


   - **Our Response:** This can be accurately modeled using professional finite element/dynamics software.


2. **Bearings in Multi-Joint Non-Linear Scissor Arms:**


   - **Question:** Do the multiple rotating joints of the non-linear scissor arm utilize traditional bearings?


   - **Our Response:** We utilize **wear-resistant nylon bearings**. This bearing technology has been proven in German machinery for 40 years, and I have personally utilized it in U.S. glass unloader systems with over 20 years of continuous, reliable operation.


3. **Cleanroom Particle Generation:**


   - **Question:** Due to strict cleanroom requirements, long-term operation must not generate particulate dust.


   - **Our Response:** We have already designed a specialized **non-linear scissor-cone dust cover/bellows**, originally engineered for robotic painting applications and fully validated by major manufacturers.


4. **Retraction Footprint:**


   - **Question:** The robot arm's retraction rotational footprint must fit within a $2\\,\\text\{meter\}$ radius.


   - **Our Response:** This is entirely achievable and can be made even smaller. Because our scissor arm features true linear extension geometry, it holds significant advantages over traditional fixed-length dual-segment jointed arms.


### 4. Insights into Existing Equipment & Our Architectural Strategy

The client showed us schematics of their currently deployed robots, revealing a notable mechanical innovation: their terminal three-segment arm uses three motors and three reducers to maintain a linear glass trajectory. Specifically, they employ a synchronous timing belt connecting the first and third axes—effectively forming an isosceles triangle where the base represents the linear path, and as the base length varies, the two base angles remain equal. While this eliminates the third axis motor, the number of precision gear reducers remains high.


#### Our Diagnostic Prescription:

> **"To boost speed, reduce weight first; to innovate, start at the end-effector."**


To enhance operational velocity and throughput, we must reduce the weight and inertia of every stage of the robot rather than merely increasing motor power. Because our **non-linear scissor-arm architecture eliminates the need for precision gear reducers in the main body**, we can first eliminate two out of six precision reducers directly at the terminal end, and subsequently scale down motor power ratings across preceding joints—establishing a systematic roadmap for **weight reduction and acceleration**.


### 5. Conceptual Design Iterations

#### Scheme 1: Symmetric Linear Scissor Arm

- Features symmetrical dual scissor-arm assemblies mounted on a central lifting column and rotation post.


- Provides intuitive force transmission and balanced extension paths, with fork ends carrying the dual-arm exchange mechanism.


#### Scheme 2: Tilted Cone-Angle Scissor Arm (Optimized Architecture)

- **Innovation:** Scheme 2 angles the non-linear arms along a semi-conical angle (e.g., a $14^\\circ$ total cone angle tilted at $7^\\circ$).


- **Feasibility:** This is viable because the non-linear scissor arm inherently operates within a fixed conical envelope during extension and retraction.


- **Advantages:** Tilting the arms allows the dual terminal ends to be **significantly more compact**, reducing the overall rotation envelope, lowering moment of inertia, and providing superior spatial rigidity through a truss-like geometry.


*Published by Smart Line Systems / SmartLai Robotics Co., Ltd.*



---
title: "Machine Learning for Congestion Management and Routability Prediction within FPGA Placement"
excerpt: "This project involved using machine learning to help with the FPGA placement problem. <br/><img src=''>"
collection: portfolio
---

Role
======
During my Master's degree I was part of the Guelph FPGA CAD Group, which consisted of faculty and students from the
School of Engineering and the School of Computer Science at the University of Guelph. My role in the group was to 
research and implement machine learning models with could help with FPGA CAD tools. As part of this research, I helped
to contribute towards a paper titled "Machine Learning for Congestion Management and Routability Prediction within
FPGA Placement."

My contribution towards this paper was to help with training some of the machine learning models alongside another 
member of the group. I was also involved in evaluating the impact multiple machine learning models had on the 
FPGA placement problems that were identified. 

Problem
======
Field programmable gate arrays (FPGAs) are chips where the hardware on the chip can be changed, or reconfigured, 
depending on the design. This allows a designer to describe a circuit, or hardware, in a programming language or by other means 
and a computer-aided design (CAD) tool transforms this description to a file the FPGA can use to configure itself.
There are multiple steps in the CAD tool which needs to be done, and one of the steps I focused on for my
research was the placement step. 

The placement step needs to find a way to place all of the components of the described circuit onto the FPGA. There are
many constraints which need to be considered to make sure the circuit can be placed. One constraint is that FPGAs only
have so many resources on them that can be used. If the design is too large, it might not fit on the FPGA. A second
constraint is the routing resources needed to connect components. The routing resources consist of wires which run throughout
the FPGA, and switches which connect these wires together. If certain components are placed too close together or too far 
away, the design might end up needing too many wires for the design, so it cannot fit on the FPGA. Additionally, if the
path between certain components is too long, the circuit may not function correctly. The routing step, which involves finding
how all of the wires and switches should be set, is done after placement and is the final step. If the placement step does not
consider the routing resources, then the routing step could fail and the placement step would need to be repeated. This 
results in both the placement and routing steps heavily relying on each other.

Because of all of the constraints and other considerations during FPGA placement,
it is a very difficult problem that can take hours or days to find a placement for large circuit designs. This slows down
the development cycle for designers who use FPGAs. FPGAs are used in many different industries and products, including
biomedical devices, defense, broadcasting equipment, and automotive vehicles.

The goal of the paper was to look at machine learning models already developed within the Guelph FPGA CAD group to
try and speed up FPGA placement without a decrease in the quality of the resulting placement. Additionally, a new 
machine learning model was developed and introduced to help improve the quality of placements.

Solution
======
In order to help with FPGA placement, some machine learning models had already been developed within the group. The two
which were used as part of this paper was a congestion estimation model referred to as MLCong and
a routability prediction model referred to as DLRoute.
MLCong is a machine learning model which takes in different features of a switch and determines how congested it is,
with congestion referring to the demand of the switch. If a lot of components need to have connected wires going through
a certain switch, it is said to be congested.
DLRoute is able to predict if a placement can be successfully routed during the routing step by
taking an image of the congestion throughout the entire FPGA at any point throughout the placement step and 
giving it to the model. This helps to determine if the placement step needs to continue further or if it can end early 
and the routing step will still be successful.

In addition to MLCong and DLRoute, a third machine learning model was developed. This model, referred to as DLManage,
manages the congestion in the FPGA placement by predicting how much to artificially inflate the size of the components
connect to a switch. The model is given an image of the congestion from any point of the placement step (this is the same
input for the DLRoute model) and the output is an array of inflation values. These inflations values represent how the
size of the components should change so components in a heavily congested area move and spread to areas with lower congestion.

These models were then used in different combinations in an FPGA placement CAD tool to see how much time can be saved by
replacing traditional algorithms with the models. While the goal was to reduce the amount of time the FPGA placement step
took to find a placement, it was still important that the placement generated did not go down in terms of quality. In order
to ensure that was the case, the total wirelength (the amount of wire being using in the FPGA) was used as a measure of quality.
The lower the amount of wirelength used, the better the placement. 

All of these models were found to have a significant impact on the placement step. MLCong is able to reduce the runtime
of congestion estimation in the placement step by 98.2%, and the congestion estimation produced is more accurate than the old
method. When DLRoute is used, it can successfully predict if parts of the placement step can be skipped. When those parts are
skipped, it results in reducing the runtime of the placement by 48% while only increasing the total wirelength in the design by 4%.
If both MLCong and DLRoute are used at the same time, the total wirelength only increases by 3%. DLManage is able to replace
part of the old congestion management techniques which needed to be tuned for different circuits. 

Impact
======
Overall, the paper was a success. It was shown that using these machine learning models can reduce the run time of FPGA placement
by 48% while still maintaining a high quality in the result. This means that FPGA designers could receive feedback on their design
faster, which would cut down the development time and costs. This research shows that machine learning can make a huge impact
in FPGA placement. The paper for this research was accepted and published in a special edition of ACM Transactions on
Design Automation of Electronic Systems.

Code/Demo/Further Information
======
Further information about the paper for this project can be found under "Publications" or by using this link: 
[Machine Learning for Congestion Management](https://szentimh.github.io/publication/2020-08-01-ml-fpga-placement-todaes-number-1).

The link to the full paper can be found here: [Full Paper](https://dl.acm.org/doi/10.1145/3373269).



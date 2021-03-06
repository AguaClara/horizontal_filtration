### Horizontal Filtration, Spring 2018
#### Clare O'Connor, Corson Chao, and Christopher Galantino
#### 5/17/2018


## Abstract
Horizontal filtration is a new innovation for the AguaClara team, arising from a desire to make the 1 L/s plants easier to make and ship through replacing the Enclosed Stacked Rapid Sand Filter. To create a horizontal filter, aspects of the sedimentation tanks and current filter design were used, such as the relationship between backwash and operational speed, as well as the design of the plate settlers. Initial experimentation with the settling of sand during upflow demonstrated the feasibility of angled plates as a method of sand retention. The team has laid a framework for future team members to modify the current model and begin the next phase in fabrication.


## Table of Contents
1. Introduction
2. Description of Apparatus
3. 1st iteration walkthrough
4. Challenges and Future Work
5. Manual
  - Special Components
  - Fabrication Details
  - Design
    - Python
    - Fusion360
  - Experiments
      - Methods
6. Appendix
  - Variables
  - Stress and Displacement Analysis


## Introduction

The AguaClara plantita (1 L/s plant) is a difficult apparatus to construct and implement. Finding a way to make fabrication, assembly, and installation simpler, as well as downsize components, will greatly decrease the cost and make the technology more accessible for global communities.

The concept of an easy to implement, versatile water treatment plant correlates nicely with the [OrigamiWaterLab](https://github.com/OrigamiWaterLab) proposed by AguaClara engineer [Ethan Keller](https://github.com/ethan92429). OrigamiWaterLab is the concept of creating an easily producible filtration system, built from easily transportable flat parts, similar creation of origami. Essentially, ingenious engineering is found in simplicity and resiliency. Fabricating a plant that transitions from flat into 3D is a innovative area of study that may become more possible with increased exploration. With more work, this concept could become a new direction for AguaClara plants.

With this idea in mind, one of the most difficult features to construct efficiently is the filter, which is both time and labor intensive to create. Currently, the 1L/s plant’s filter is characterized by a vertical, enclosed stacked rapid sand filter (EStaRS) which is tall and cumbersome to ship in addition to having a complicated geometry of 4 inlet manifolds and 3 outlet manifolds.

To combat these difficulties, the horizontal filtration team has proposed a horizontal filter design. This filter will not be stacked. Instead, it will use horizontal flow for filtration and vertical flow for backwash. The ratio of the horizontal flow area to the vertical flow area will be designed so that the bed will fluidize during backwash. The inlet and outlets will be designed so that sand/water separation doesn’t require slots. Additionally, this innovation in the horizontal filter could ultimately eliminate the need for slots on the OStaRS (Open Stacked Rapid Sand) filter, as is used in the full-size AguaClara plants. In the horizontal filter, water will enter and exit through a geometry that has a plate settler style design to ensure that sand settles out and isn’t carried into the effluent. This design for the horizontal filter will utilize both current filtration techniques and technologies from the plate settle design in the sedimentation tanks.

The goal is that these design innovations will simplify the current design and facilitate scale-up and mass production of AguaClara technologies.

## Design of Apparatus

The horizontal filter uses concepts and designs from current AguaClara technology in sand filtration. This section will outline the general function of the apparatus in its most current design. This includes the concepts behind specialized components as well as justification for several of the design choices.

*The "1st iteration walkthrough" section follows the fabrication of an outdated model of the horizontal filter. Since its creation, new designs were incorporated into the final apparatus described in this section as a result of items learned during the 1st iteration process and revisiting troubling concepts.*

At a basic level, sand filtration involves running water through a bed of sand. Often this is done in the vertical direction; however, the total volume of the filter could be decreased if forward filtration is run horizontally and only backwash is run vertically.  Figure 1 shows the simplest schematic of this process with water flowing horizontally in a bed of sand between two plates.

<center>

| <img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/water_movement.JPG?raw=true" size = 400px >|
|:----:|
| Figure 1 : The flow of water through the horizontal filter. Water enters through the inlet and travels across the sand bed toward the outlet. This is forward filtration.|

</center>

To permit the flow of water from the inlet channel to the outlet channel, a series of slits line the body of the plates. See Figure 2 for a Fusion360 rendering of slit placement. The number of slits was determined based on the necessary spacing of the holes with respect to the headloss constraints of the system, which will be described later in reference to the filter shelves, with complete calculations in the "Manual" section.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/plates_with_slots.JPG?raw=true" style="width: 350px;" >|
|:----:|
| Figure 2: The entrance and exit plates are perforated with slits in order to permit forward filtration.|

</center>

Also within the entrance and exit plates is a part of the apparatus referred to as the filter insert. The filter insert consists of two components: center plates and filter shelves. As a whole, the filter insert acts to keep the sand within the main body of the filter.


| ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Filter_shelf_labelled.JPG?raw=true" style="width: 450px;" > |
|:------------:|
|Figure 3: The filter insert serves to keep sand within the main body of the filter. It is composed of three center plates and filter shelves.|


Similar to the design of the AguaClara sedimentation plate settlers, the filter shelves exist to provide a place for any sand that has been lifted to settle rather than being carried out of the filter. The shelves are narrow strips of acrylic which are notched, as shown in Figure 4. They are placed at an angle and slanted by 60 degrees on the top lip to fit flush along the faces of the entrance and exit plates. The lip serves as a precautionary measure for the trapping of sand in the frame of the filter if sand were to reach this area. The spacing of the filter shelves was determined from an allowable headloss as well as allowable sand lift (see "Python"). To avoid issues with the flow, shelf spacing needed to be much less than the distance across the filter.

| ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Filter_shelf.JPG?raw=true" style="width: 350px;" > |
|:------------:|
|Figure 4: A filter shelf. The component is notched for a snug fit within the center plates without the need for glue or welding. |

The center plate is the structure that supports the filter shelf. It has notches which complement the notches on the filter shelves. This ensures the shelves and the center plates fit together well and will not wiggle during operation. Three center plates, as seen in Figure 6, are in the design to provide the most stability for the shelves.

| ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/filter%20shelf.JPG?raw=true" style="width: 300px;" > |
|:------------:|
|                     Figure 5: The center plate component. It contains notches to complement the filter shelves.|


| ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/3shelf.JPG?raw=true" style="width: 350px;" > |
|:------------:|
|                     Figure 6: Three center plates characterize the filter shelf insert. This provides optimal stability for the filter shelves. |

When combined, the filter shelves and center plates form a removable component known as the filter insert which can be easily put in and taken out of the filter box. This is a beneficial quality for maintenance purposes. A rendering of the insert location can be seen in Figure 7, first complete and then with the entrance plate removed so the configuration of the shelves is visible.

| ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Horfi_updated.JPG?raw=true" style="width: 300px;" > |
|:------------:|
| Figure 7: This image shows the placement of the filter insert within the filter box, specifically between the entrance and exit plates. The top image shows this system complete, while the bottom images shows the filter with the entrance plate removed to better show configuration of the shelves in relation to the rest of the box. |

As mentioned before, water enters through the inlet and seeps into the sand bed via the entrance perforated plate. From here, water moves from left to right (when viewed cross-sectional). Particles are gradually removed from the influent as the fluid experiences forward filtration. Once water reaches the other side, it leaves through the outlet for its distribution.  

Notice the filter gates, colored orange in Figure 8. These will be important during the backwash step mentioned later in this section.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Overall_function.JPG?raw=true" style="width: 350px;"  >|
|:----:|
| Figure 8: A cross-sectional view of the flow of water through the horizontal filter. The horizontal filter is composed of entrance and exit filter gates, entrance and exit plates, an internal filter insert with filter shelves, and a siphon/gasket system.|
</center>

To stop the escape of sand out of the slits in the entrance and exit plates, the filter shelves serve their intended function. The idea behind the filter shelves is to provide an opportunity for the sand to settle should it be lifted during either forward filtration or backwash. As seen in Figure 9, water flows in and out while carrying some sand with it. To combat this, the shelves allow a surface for the sand to settle and promote the recirculation of sand within the filter. In experiments, which are detailed in the Appendix, the understanding that this is what happens was confirmed.

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/filter_shelf_function.JPG?raw=true" style="width: 500px;">|
|:----:|
| Figure 9: A close-up of the filter shelf in action. The routine movement of water through the filter has the potential to bring sand with it. In turn, the filter shelf provides an area for the sand to settle and be returned back into the sand bed.|

</center>

During backwash, the process of cleaning the filter, several other components must be incorporated into the filter. Figure 10 shows the addition of these parts. Firstly is the siphon, shown in grey, which is located on the top of the filter. The siphon initiates backwash by creating low pressure within the sand bed. To prevent water from continuing to come in from every slit on the inlet plate, backwash gates close off all the slits except for the one on the bottom on the inlet side, and also closes all the slits on the exit side. This process requires more water to flow from the bottom hole and up through the sand bed at a higher velocity than during forward filtration. The higher velocity produced in this process perturbs the sand and rinses away smaller particles from the sand. This effluent is discarded. Upon completion of backwash, the siphon is closed and forward filtration resumes.

<center>

|  <img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Backwash_steps.JPG?raw=true" >|
|:----:|
| Figure 10: In Step 1, water is being filtered in its routine fashion. When the filter becomes saturated with removed particles, the apparatus experiences an increase in headloss and has difficulty functioning. To solve this, the siphon is activated (Step 2). The filter gates are pulled inward due to this vacuum effect and water can only flow through the bottom. This upflow of water causes the sand bed to fluidize, separating the sand from filtered particles in the process and thus cleaning the filter. These particles leave through a launder pipe (not shown) at the top of the filter box for proper disposal. Forward filtration may then resume.|

</center>

As seen in step 2 of Figure 10, water flows from an uncovered bottom inlet slit and through a triangular space before moving into the sand bed for the fluidization step. This zone is shaped intentionally as such and is enclosed by what the team calls the bottom shelf. The bottom shelf inserts into the bottom most center plate notch from Figure 5. The bottom shelf creates a gap at the bottom of the filter system which makes a predetermined space for influent to go through.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/bottom_shelf_function.JPG?raw=true" style="width: 350px;" >|
|:----:|
| Figure 11: The bottom shelf creates a gap for influent to surge through a predetermined point.   |

</center>

The bottom shelf stretches across the entire width of the filter. It serves to control headloss at this point as well as prevent dead zones during backwash by provoking a more vertical initial upflow out of the inlet. Due to its predetermined shape, the headloss due to the inlet condition is easily determined and can be used to understand the restrictions on backwash.

Like the filter shelves, the bottom shelf also has an angled lip that rests against the entrance plate. This can be seen in Figure 12.
<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/bottom_shelf.JPG?raw=true" style="width: 350px;" >|
|:----:|
| Figure 12: The bottom shelf follows the same notching scheme as the filter shelves. It acts as the bottom most inserted component of the filter shelf.|

</center>



Another important aspect of the current design (May 2018) are carved channels in the center plate design. These carved channels allow the free flow of water along the entrance and exit plates. The overall shape and location of these filter shelves may be seen in Figure 13.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Insert_Assembly_channels.JPG?raw=true" style="width: 350px;" >|
|:----:|
| Figure 13: The location of the carved channels along the filter insert. These channels allow the free flow of water along the entrance and exit plates.|

</center>

It is important for water to be able to flow freely during routine forward filtration because the center plates are not equally spaced in the filter insert. Therefore, preferential flows were a resulting factor that the team had to eliminate as a variable. Figure 14 shows the theoretical ability of influent and effluent to flow in an unconfined width.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/carved_channels.JPG?raw=true" style="width: 550px;" >|
|:----:|
| Figure 14: Carved channels in the center plates located against the entrance and exit plates allow the free flow of water during routine forward filtration.|

</center>

The components and relationships discussed in this section is the extent in which the team has designed and considered thus far. See "Challenges and Future Work" for more details on tentative plans for the coming semester.

## 1st Iteration walkthrough

*The following section describes the first iteration of the horizontal filter. Upon it's construction, the team determined that further iterations would be needed to build a filter with components that are more precise and consistent. In response, the team designed a full Fusion360 model of the filter assembly, on which the next iteration will be based. This Fusion360 link has been attached in the Manual of this report and includes current and past designs. This section is meant to be stand alone and tells the story of how the explanation of the apparatus will focus on the challenges with this design and the changes that were made in the updated design.*


#### Design

As an overview, the horizontal filter consists of 4 main parts: the acrylic box, the entrance/exits plates, filter shelves, and the center plates. In Figure 15 below, each of those parts are labelled.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/labeled_real_box.PNG?raw=true" style="width: 450px;" >|
|:----:|
| Figure 15: This is a photo of the apparatus as currently constructed. Notice the differences between this fabricated model and the modifications that have been made in the current design as of May 2018.|

</center>

  -   **Acrylic Box:** The box was bought premade from a website (See list of parts below). It has a thickness of 1/4" and its size is the overarching constraint of the filter design.
  - **Entrance and Exit plates:** In the side-view image (Figure 15), the entrance and exit plates are only minimally seen. Though not yet constructed in reality, a thickness of 1/4" will be sufficient for these walls.
  - **Filter Shelves:** In the 1st iteration, there are 36 filter shelves which act as retaining plates for the sand in the filter by providing a surface for the sand to settle on to and by blocking the exit holes. As built, the plates are angled at 60 degrees from the horizontal with an angle cut underneath on the outside edge to help the shelves fit more snugly against the inside walls of the entrance and exit plates. At angles steeper than 60, this additional cut proved impossible to fabricate. In the updated design, the shelf angle was changed to 55 degrees so that the additional lip angle would be possible (see "Design of Apparatus" for more information on this). In addition, the space constraint of the shelves changed slightly with this change in angle so that, in total, there will be fewer shelves on each side. The first iteration construction of the shelves is shown in Figure 16.

<center>

|<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Shelf_creation_combined_photo.JPG?raw=true" >|
|:---:|
|Figure 16:  See Manual for more details on the drilling and cutting method|

</center>

  - **Center plates:** The center plates support the filter shelves. As built, two center plates were used to separate the filter into three sections. In the new model, there are three center plates; one in the center and two that are 1" from the side of the box. Notches are cut in the plates to allow the filter shelves, which are also notched, to fit together without coming loose. Using three plates instead of two prevents the shelves from warping and developing an uneven spacing as seen in Figure 15. In addition, channels are to be cut out to allow water to run between the sections in the filter and in the channels under each shelf. This can be seen with more description "Design of the Apparatus."

<center>

|<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/shelf_holder_construction.jpeg?raw=true" >|
|:---:|
|Figure 17: The construction of the center plates. With the measurements drawn onto one center plate template, the other could be clamped underneath to ensure a consistent cut.

</center>

  - **Filter Insert:** The filter insert assembly, as seen in Figure 18, is the combination of the center plates and the filter shelves. The center plates are characterized by angled notches that provide a pathway for the filter shelves to slide into. Note the acrylic shelves; these 1/8" thick components, although brittle, will be used in future iterations because they are a cheap alternative to PVC. This will lower the overall cost of the filter.

  <center>

  |<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/inserting_shelves4.jpeg?raw=true" >|
  |:---:|
  |Figure 18: Construction of the filter insert. The filter shelves were inserted into the notches of the center plates.|

  </center>


#### Additional parts  
  Several additional parts will be necessary to develop once the filter in forward operation is functional. One of these is the **siphon system**. The siphon is used to initiate the upward flow in the filter. While designing a siphon isn't difficult on its own, the challenge will come from sealing it into the top of the box while also maintaining the ability to adjust the filter insert should maintenance be necessary. This need will require a robust **gasket system**, which is the other major additional component of the system. To seal the edges of the plates within the tank, a gasket will be necessary as well, but given that that gasket will be static within the system it should be simpler to design than the top backwash gasket.

## Challenges and Future Work

As the Horizontal Filtration team continues, fabricating the updated design will be priority. This will include creating a jig, from which the filter shelves and center plates can be constructed, as well as using a CNC machine to make the entrance and exit plates. From there, adding EPDM foam gaskets will allow tests of the system in forward filtration mode. After success in forward filtration, efforts can be made to develop the components for backwash, most importantly the siphon system and the backwash doors (filter gates). Developing an adequate seal in the doors is likely to be the largest challenge. Further work beyond backwash could go into constructing the system so that the siphon valve is connected to the backwash doors; making it easier to operate.


# Manual
This section outlines fabrication and component details not otherwise specified in the body of the report.

## Special Components

**Acrylic Box:** An acrylic container of specifications 18x18x24" bought from [Shop Pop Displays](http://www.shoppopdisplays.com/P_PED-ACRYLIC-CLEAR-FLAT/clear-acrylic-pedestal.html) in order to act as an observable, smaller model of the designed horizontal filter.

**Ethylene Propylene Diene Monomer Rubber (EPDM):** Sheets of EPDM will be used as seals to cover the slits in the entrance and exit plates during backwash. EPDM will also be used in maintaining water tightness when potentially using gaskets for sealing. (obtained through *McMaster-Carr*)

**PVC Sheets:** Sheets will be cut into the forms of the shelves, entrance/exit plates, and the filter shelf holders. (obtained through *McMaster-Carr*)

**Aluminum Angle Iron:** Stabilizer for one version of the gasket system. This gasket system may be out-dated by next semester. (obtained through *McMaster-Carr*)

**1/8" Router Bit:** Router will be used to cut holes in PVC (obtained through *McMaster-Carr*)

**Stainless Steel Phillips Screw, Washer, Split Lock Washer, Hex Nut:** These components will be used to fasten the gasket system securely to the tank. (obtained through *McMaster-Carr*)


## Experiments


To determine the initial parameters, the team conducted several experiments with the flow of water in relation to the sand. These experiments were done to verify hypotheses when calculations (see "Python") did not yield conclusive answers, specifically to determine the length of the filter shelves based on how sand settled in angled tubes of different diameters.

#### Methods

A tube was used to simulate the main body of the filter with a smaller, angled tube branching off the main body. The outlet branch allowed the team to measure how far sand would rise in the outlet, which could inform the length of the filter shelves given the velocities expected in the filter. Additionally, an understanding of the speeds required to drive sand into an outlet could further inform aspects of the OStaRS, specifically the necessity of the slotted pipes.

###### Experiment: 1" and 1/8"
1. First, a mock filter was constructed using a 1" clear PVC pipe; in this pipe an angle hole was drilled at 45 degrees from the vertical around 5 inches from the top of the pipe. Into this hole, a small length of 1/8" tubing cut on one end to an angle of 45 degrees was inserted and glued. See Figure 19.
2. Dry sand was poured from the top into the apparatus to see if dry sand would move up the outlet tube when the sand level was two inches above the angled outlet. It did not.
3. An additional 500 g of sand were poured in increments of 100 g, this corresponded with an additional height of about 1.5 ft in the 1" pipe. At no point did dry sand enter into the outlet tube.
4. Water was then slowly added into the original amount of sand. During this process, water carried sand into the first inch of the outlet tube.
5. Pumps were checked for proper flow rate to get the appropriate water velocity in the outlet tube corresponding to the outlet diameter and speed required for backwash and operation speed. The water within the body of the filter was moving at a speed required for backwash (9 mm/s) and the outlet was pulled at the speed required during operation (1.8 mm/s) as that should be the maximum velocity experienced in the filter shelves.
6. Water was then pumped through the wet sand. Sand moved around 3 inches up the length of the outlet tube. Preferential flow paths were observed as the apparatus was tilted.

<center>

|  ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/small_diameter_outler.jpg?raw=true" style="width: 300px;" >|
|:--:|
| Figure 19. The first experimental apparatus with 1" diameter filter and 1/8" outlet tube. Influent water comes in through the bottom and out through the angled outlet and the top. |

</center>

###### Experiment: 1" and 3/4"

1. Originally, the plan had been to use 1" and 1" but fabrication of the experimental apparatus was extraordinarily challenging, so the outlet tube dimension was changed to reflect what was possible to construct. Because of this a 3/4" inch pipe was used instead. Using a drill press with a hole saw attachment, an angled hole was drilled into the main 1" tube. The 3/4" pipe was then cut on one end with the same size hole saw bit. This meant that the curvature of each piece fit together more snugly than had the 3/4" pipe been sliced flat. The two pieces were welded together.
2. Sand was poured into the container to a level of around 4 inches above the opening of the angled outlet. Sand moved slightly into the angled tube.
3. The apparatus was filled with water, and the inlets and outlets were hooked up to their respective pumps and waste lines. At this point the sand rose in the outlet column to a length of around 3 inches.
4. The pumps were reset to work at the new speeds needed to pull water through the outlet at 1.8 mm/s and through the main filter at 9 mm/s. As the sand in the main column fluidized, the sand dropped in the outlet column to a length of 1.1" which remained constant over the several minutes that the pumps were on.
5. The pumps speeds were altered away from what would be useful during operation to develop a sense for what effect that could have on the proper function of the filter shelves. Below is a table of the values obtained.

<center>

| ![]()<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/one_inch_outlet.jpg?raw=true" style="width: 300px;" >|
|:---:|
| Figure 20. The second experimental apparatus with 1" diameter filter and 3/4" outlet tube. Influent water comes in through the bottom and out through the angled outlet and the top.|
</center>


<center>

#### **Table of  pump speed and sand length in outlet tube**
|filter speed (RPM)|outlet speed (RPM)|sand length in tube (in)|
|:---:|:----:|:----:|
|73|11.4|1.1|
|80|11.4|1.1|
|50|11.4|1.1|
|87|11.4|1.05|
|73|15|1.5|
|73|19|1.95|
|73|23|4|
|73|11.4|1.1|
</center>

From this data, it is apparent that changing the speed that the water is being pulled out affects the height of sand in the filter shelf but changing the overall flow does not. This makes sense since any water not pulled from the outlet increases the flow through the unregulated outlet. With the proper pump speeds of 73 RPM for the influent and 11.4 RPM for the effluent, the length the sand travels into the outlet (1.1") is a small enough distance to make the actual construction feasible. The influent and effluent speeds differ due to the actual model having multiple holes to create outflow. However, in this one hole model, the amount that would be measured going into the other holes was just left as waste outflow rather than along with the effluent. The python code in the Python section explains the significance of these values and how they were determined.

## Fabrication Details


###  Initial Filter design

1. **Center plates:** the center plates were cut to shape using the band saw. The slits were cut by making 1/8" holes using the drill press, with the 1/8" chosen as it is the thickness of the filter shelves. Drilling the holes made it possible to keep a fairly straight cut to the proper depth while avoiding the problem of having two cuts and no way to get the middle out. The location of the holes and the angle of the cut was pre-drawn onto the PVC. In future iterations, it is recommended that a stencil be cut out and the plates be cut using a CNC Router to follow the stencil. This will likely provide more control and uniformity between cuts.
<center>

|<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/Hole%20cut.JPG?raw=true" >|
|:---:|
|Figure 21: This sketch illustrates the fabrication method used to cut notches in both the center plates and filter shelves. The blue circle was drilled out first, then two cuts parallel to the outer edges of the hole were made using the band saw. This technique left a rounded notch in the plates, but maintained a decent degree of consistency over made cuts.
</center>


2. **Filter shelf:** The filter shelves were cut from a sheet of 1/8" acrylic. To cut the notches into the shelves, the same technique used for the center plates was used but varied for the difference in thickness. First, a 1/4" hole (corresponding to center plate thickness) was drilled at a measured location on the shelf with the drill press. The location of the notches depends on the number and location of the center plates. In the built model, this was chosen to be at the 1/3 and 2/3 distances along the width of the shelf to create 3 even sections. Upon drilling the holes, the notch was cut using the band saw. To get the angled lip of the filter shelf, a jig was constructed first by the team and later by Tim Brock of the machine shop. The jig provided an angled surface to attach the shelf to as it was fed through the band saw. This process required much precision and care. While it worked, potential other methods of shelf fabrication should be explored. One option is to cut the shelves at an angle as a first step to avoid needing to shave thin strips after holes have been drilled. This would save time, would be less wasteful, and ensure better safety for team members.

|<img src="https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/jig.JPG?raw=true" >|
|:---:|
|Figure 22: This picture shows the convenience and added accuracy of using a jjig to cut the slanted edge on the filter shelves. Cuts were made smoother and more consistent along with streamlining the process. For the next iteration, more jigs will be made for faster, better fabrication

3. **Entrance/Exit Plates:** Currently, the entrance and exit plates are only fabricated so they fit into the acrylic box. The main plates were cut in the machine shop using the large bandsaw and sanded so they would sit flush in the box. The team expected a change in methods and decided not to proceed with cutting the holes.

### Preliminary Gasket work

Some work was started on designing the gasket system for the filter. Aluminum Angle Iron was cut and drilled, as was EPDM rubber. This process proved unreliable as a fabrication method for several reasons such as inexperience with the materials, incomplete Fusion360 design, and imprecise methods. This could be seen in one method which involved freehanding a cut in the EPDM while it was held down by several clamps. More exploration in this area will be done. One potential option is to use EPDM foam rather than EPDM. EPDM foam is a rubbery foam that may compress more evenly with fewer components. However, it will need to be purchased and tested for ease of use as well as water tightness.

## Design

#### Filter Functionality: A Summary
The purpose of this filter assembly is for simplicity and easy fabrication. The filter exists within an acrylic box with an inflow and an outflow as the empty cavities that do not contain the sand filtering section. The sand column section itself exists in the middle of the filter box with a filter shelf insert that may be added or removed. While the filter gates are open, water flows in through one side, experiences sand filtration, and then exits out the other side as clean effluent. The angled components within the filter bed are the filter shelves which serve to keep sand out of the influent/effluent channels.


#### Python
The team first calculated the dimensions of the sand filter space which make up a section of the overall apparatus. To do this, the team took into account the velocity at which water moves through a sand filter and the desired flow rate of the system. As the goal was to create a model, the size constraint on the filter was determined by what size box would be easy to use. This constraint resulted in a filter with a 0.37 L/s flow capacity.

Since the backwash velocity is significantly greater than the filter velocity (as the volumetric flow is the same while cross-sectional area is less) it is the principal design constraint. With some math, the area of backwash and area of flow may be calculated.

```python
from aide_design.play import*
V_filter = 1.8*(u.mm/u.s)
V_backwash = 9*(u.mm/u.s)  #the constraining velocity
Q_plant = .37*(u.L/u.s)  #the scale we are working with for our first iteration of the filter, manipulated to achieve desired width
A_backwash = Q_plant/V_backwash #plan view area of sand (x,y axis)
A_flow = Q_plant/V_filter  #cross sectional area of sand (x,z axis)
```
From here, the team incorporated some knowledge on the depth in which water travels through a traditional AguaClara Open Stacked Rapid Sand (OStaRS) filter. The filter backwash ratio is the ratio between settled sand height during filtration and expanded sand height during backwash. Because the filter backwash ratio is 1.3 (PiFiBw), which has been empirically determined, the team determined a settled sand height first.

The team decided that with the scale model in mind, 3.65 inches of sand in the flow direction (filter_length) is a fair parameter to start with. 3.65 inches was chosen through variable manipulation. In the code below, filter length was changed accordingly to optimize the size of an acrylic tank that could then be purchased for the scale model. With this one measurement and the ratio between filter velocity and backwash velocity, all other parameters fall into place.

```python
PiFiBw = 1.3
filter_length = 3.65*u.inch  #manipulated to achieve desired height
filter_width = A_backwash/filter_length #the filter width is the width for BOTH areas
filter_height = A_flow/filter_width
filter_height #height of sand
box_height = filter_height*PiFiBw #the height the expanded sand bed
box_height
#the box we ordered is 18 inch by 18 inch by 24 inch with wall thickness of 0.25 inches
print(box_height.to(u.inch)) #must be 0.25 less than actual because of thickness of the box floor ordered
print(filter_width.to(u.inch)) #must be 0.25*2 less than actual because of thickness of walls on either side
print('The height of the tank should be at least',box_height.to(u.inch),'with a cross-sectional width of',filter_width.to(u.inch),'(thicknesses omitted).')
>>> height is 23.72 inches, cross sectional width of 17.46 inches
```

From here, the team worked to calculate and parametrize the filter shelf insert. The calculations in this section consist of the steps used in calculating the filter shelf length. That is, how far into the filter they must protrude.

The number of filter shelves to add is determined by the distance between respective shelves. This will be optimized by investigating how far sand will travel before settling on the plates due to the velocities of this system. This was performed experimentally (see "Experiments") as well as theoretically below. The team considered both laminar and turbulent settling velocity situations.

Below is the equation for terminal settling velocity where d is diameter, $\nu$ is kinematic viscosity. This is used for laminar flow.

$$ Vt = \frac{d^2g}{18\nu}(\frac{\rho_{particle}-\rho_{H2O}}{\rho_{H2O}}) $$

After consultation with Professor Monroe Weber Shirk, it is necessary to also make calculations with turbulence in mind since sand settles rather quickly and experiences drag.

$$ Vt = \sqrt{\frac{4g}{3Cd}\frac{\rho_{sand}-\rho_{H2O}}{\rho_{H2O}}}   $$

```python
SF =2 #safety factor suggested by AguaClara Engineer Ethan Keller

rho_sand = 1602*u.kg/u.m**3 #density of sand
rho_water = 1000*u.kg/u.m**3 #density of water at 20 C
nu_water = (pc.viscosity_kinematic(293*u.K)) #kinematic viscosity of water at 20 C
d_sand = 0.5*u.mm #diameter of sand particle
alpha = 55*u.degrees #angle of filter shelves
V_alpha=1.8*u.mm/u.second
 #filter speed!

V_actual = V_alpha/np.cos(alpha) #speed within the angled shelf
S=(1*u.inch).to(u.mm) #distance between shelves (above or below)

V_settling1=((d_sand**2)*pc.gravity/(18*nu_water))*((rho_sand-rho_water)/rho_water)
V_settling1.to(u.mm/u.s)  #settling velocity (Vt) without drag and turbulence
>>>82 mm/s
V_capture1 = V_settling1/SF #Capture velocity with safety factor incorporated
V_capture1.to(u.mm/u.s) #initial capture velocity
>>>41 mm/s

Re = (V_backwash)*(1*u.inch)/(nu_water)
Re.magnitude #Reynold's number for drag coefficient calc
Cd = 0.2 #drag coefficient corresponding with ~10^7
V_settling2 = np.sqrt(((4*pc.gravity*d_sand)/(3*Cd))*((rho_sand-rho_water)/rho_water))
V_settling2.to(u.mm/u.s)
>>> 140 mm/s #this velocity uses the drag coefficient based of the Reynolds number
V_capture2 = V_settling2/2
>>> 70 mm/s #alternative capture velocity

L1 = ((V_actual*S/V_capture1-S)/(np.cos(alpha)*np.sin(alpha)))
L2 = (S/np.cos(alpha))*((V_actual/V_capture2)-(1/np.sin(alpha)))
L1.to(u.inch)
L2.to(u.inch)
>>L1 = -1.96 inches
>>L2 = -2.05 inches
```
These lengths and their negative values made the team believe that the length of the filter shelf is arbitrary due to their negative value. This seemed to correlate with the experiments as well in that at normal operating velocities, the actual settling velocity does not matter (see "Experiments"). Therefore, the team decided to calculate filter shelf length, and in turn filter shelf insert length, by other means. The code below explores this method.

```python
#the team decided that the diameter of a hole should be 0.25 inches and we worked from there.
space_shelf = 0.25*filter_length #this relationship was determined by Monroe as a reasonable measure. space_shelf is the total space between respective shelves. It is the same thing as L_vert.
>>space_shelf = .9125 inches (2.318 cm)

diam_holes = 0.25*u.inch
num_holes = filter_height.to(u.cm)/space_shelf.to(u.cm)
>>> num_holes = 20

#what is the headloss? (due to wall in middle of insert, there will be twice as many holes)
pi_orifice = 0.62
headloss_hole= pc.head_orifice(diam_holes,pi_orifice,Q_plant/(2*num_holes))
>>>headloss_hole = 1.13 cm

thickness_shelf = 0.125*u.inch #acrylic shelf
space_sandlift = 1*u.cm  #space_sandlift was a guessed value of a safety for how high the sand would climb in between adjacent plate shelves
space_above_hole = space_shelf-diam_holes-thickness_shelf/np.sin(alpha)-space_sandlift
space_above_hole.to(u.cm)
>> space_above_hole = .2952 cm #space above hole
L_vert = (diam_holes+thickness_shelf/np.sin(alpha)+space_sandlift+space_above_hole)
L_vert.to(u.cm)
>>>L_vert = 2.3177 cm
L = L_vert/(np.sin(alpha))
L.to(u.cm)
>> L = 2.82945 cm #length of filter shelf
L_notch = L/4 #for support of the material
>> L_notch = .70736 cm

L_horizontal = L*np.cos(alpha)
>> L_horizontal = 1.62291 cm

insert_length = 2*L_horizontal+filter_length
>> length_insert = 12.517 cm
```
From these calculations and the given constraints, the length of the filter shelves is 2.829 cm and the length of the insert is 12.517 cm. With these values, the overall apparatus could be fabricated in Fusion360 (see "Fusion360").

Depending on the length of the filter insert assembly, the spacing of the plates would be adjusted accordingly. This is due to the fact that the length of the filter insert, as set by the length of the filter and flow constraints, determines how far apart the entrance and exit plates need to be. The idea is that they would be fully secured once the apparatus is in use and only the insert would remain removable.

#### Fusion360

Our [Fusion360](https://cornell47.autodesk360.com/g/projects/20180202115885156/data/?tryNew=true) repository

The Fusion360 project linked in this section consists of iterations of the Horizontal Filter as well as older renditions of specific components, which are up to date as of May 17th, 2018. Images of the filter may be found in the "Design of Apparatus" section of the report.


# Appendix

### Variables
- **A note on the coordinate system**: "length" is used to mean parallel to flow direction. For example, filter length is the horizontal distance the water flows within the sand section of the filter. "Width" is the direction perpendicular to flow direction; center plates are spaced along the width of the filter. Height is the vertical direction.

##### Calculation of Backwash and Flow Area
- $V_{filter}$=***V_filter***=Velocity of filtration
- $V_{backwash}$=***V_backwash***=Velocity of water during backwash
- $Q_{plant}$=***Q_plant***=Water flow through plant
- $A_{backwash}$=***A_backwash***=Area of backwash
- $A_{flow}$=***A_flow***=Cross sectional area of sand/area of flow

##### Calculation of Filter Box Dimensions
- $\pi_{FiBw}$=***PiFiBw***=Volume increase ratio due to sand bed fluidization
- $l_{filter}$=***filter_length***=Length of filter
- $w_{filter}$=***filter_width***=Width of filter
- $h_{filter}$=***filter_height***=Height of entire filter
- $h_{box}$=***box_height***=Height of utilized box model

##### Calculation of Necessary Filter Shelf Length
- $\nu$=Kinematic viscosity
- $\rho_{sand}$=***rho_sand***=Density of particle
- $\rho_{water}$=***rho_water***=Density of water
- $\nu_{water}$=***nu_water***=kinematic viscosity of Water
- $d_{sand}$=***d_sand***=Diameter of sand particles
- $SF$=***SF***=Safety factor
- $\theta_{settling}$=***angle_settling***= Angle of filter shelves
- $V_{setting}$=***V_settling***=Velocity until the sand settles
- $V_{capture}$=***V_capture***=Safe estimate of velocity needed to capture the sand
- $V_{\alpha}$=***V_alpha***=Filter speed
- $V_{actual}$=***V_actual***=Filter speed after filter shelf
- $\alpha$=***alpha***=angle of shelves
- $l_{shelf}$=***L***=Length of filter shelf

##### Filter Shelf Dimension and Spacing Calculations
- $d_{shelf}$=***space_shelf***=Spacing between filter shelves (top to top)
- $d_{holes}$=***diam_holes***=Diameter of the holes in walls
- $N_{holes}$=***num_holes***=Number of holes on either side
- $\pi_{orifice}$=***pi_orifice***=Shrinking coefficient of water through area
- $h_{hole}$=***headloss_hole***=Headloss through the hole
- $t_{shelf}$=***thickness_shelf***=The thickness of the shelves
- $d_{sandlift}$=***space_sandlift***=Safety factor for sand to lift
- $d_{abovehole}$=***space_above_hole***=The spacing between the hole and the bottom of the Shelf
- $l_{vert}$=***L_vert***=Spacing between shelves, top to top=***space_shelf***
- $l_{shelf}$=***L***=Length of filter shelf
- $l_{notch}$=***L_notch***=Length of the notch into the filter Shelf
- $l_{horizontal}$=***L_horizontal***=Length of horizontal component of filter shelf
- $l_{insert}$=***insert_length***=Length of the filter insert to which the filter shelves are connected

### Stress and Displacement Analysis

In order to see how plausible this design is, a stress test was performed on the acrylic box with the expected hydrostatic forces in mind. This is a function feature found in Fusion360

<center>

|![stress_test](https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/stress.PNG?raw=true)|
|:---:|
|Figure 23: Stress forces on the acrylic box during operation.|

</center>

This stress analysis could then be translated into an approximate displacement of the box itself.

<center>

|![displacement](https://github.com/AguaClara/horizontal_filtration/blob/master/Spring%202018/images/displacement.PNG?raw=true)|
|:---:|
|Figure 24: The displacement of the box walls during operation.|

</center>

Since the walls would only flex a max of 2.88 mm, the design is structurally sound.

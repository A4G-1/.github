<p align="center">
<img src="https://firebasestorage.googleapis.com/v0/b/share-ff6c6.appspot.com/o/logos%2FSharePool%20(7).png?alt=media&token=77c0cf20-edc8-4b47-820e-f77fe941af87" align="center" width="500">
</p>

# Executive Summary

Currently, students are unable to commute to school due to issues with services that provide transportation. Buses tend to be late or systems are entirely defunct. As a result, there needs to be a method for users to arrive to and from school without relying on a bus system. However, services such as Uber and Lyft come at high costs. As a result, SharePool presents a novel solution by enabling users to plan routes together without the interference of another third party business. Users can plan based on their schedule and start and end routes with other students or friends. Our app will specifically allow students to arrive at school in amore timely fashion and allow parents to plan pickup in carpool groups.

# Introduction

— I. Problem —

In the present, it is highly difficult for users to plan carpools together. In order to rideshare, most people tend to utilize services such as Uber or Lyft in order to travel from one location to another. This trend turns into an issue in the scope of commuting to school. When commuting to and from school, using a service such as Uber is not feasible in the short timespan that students have prior to arriving at school. This dependency forces students to rely on bus systems, a network which also contains several flaws.

The main issue arises with the pricing of buses as they tend to cost far more than some students can afford. In California, the $40 bus fee has prevented some students from being able to attend classes, leading to the possibility of being unable to graduate from college (West, 2021). When the commute to school becomes an obstacle towards graduation, it becomes clear that an alternative must be identified to enable more individuals to graduate.

Furthermore, this issue extends to highschoolers as Chalkbeat reports that “Two-thirds of Detroit students missed at least one of every 10 school days in 2021.” Detroit faces this issue due to a system of inadequate transport planning with buses. As a result, the responsibility to arrive to and from school falls on the shoulders of parents and family friends (Chalkbeat, 2023). Missing school due to the inability to transport prevents students from receiving valuable instruction. 

Aside from high prices and bus systems that are defunct, experts find that transport systems that are in place still tend to cause issues. In New York City, 350 buses are late every single day in varying districts (New York City Council, 2022). Thus, in this scenario, students are able to arrive at school, but they miss valuable time from instructors. In order to ensure students can graduate and have successful futures, these issues must be alleviated.

— II. Audience —

The primary users of this application will be students and parents. Since transportation is an issue for both middle/high school students as well as undergraduate students, the application will be used for both demographics. In the United States, it is illegal for students to drive until they turn 16, so the student and the parent will both download the application and use the functionality in order to plan and manage ride sharing. However, at the undergraduate level, because students are at an age where they can legally drive, students will typically be the ones in charge of ride sharing and planning.

In order to solve the problems mentioned in section I, the main goal for our application is to (a) provide users with a low-cost method to arrive at school, (b) arrive at school on-time without missing instruction, (c) streamline school carpooling with estimate time of arrival and other built in features. As previously mentioned, students in Detroit and New York City often miss instruction due to faulty bus systems. Goals a and b solve for these issues. Furthermore, students unable to use the bus system due to costs will now be able to use our application to arrive to and from school at no cost. Our third goal provides an extra measure of safety and reassurance to both students and parents alike.

— III. Competition — 

In terms of ridesharing, the first competitors in the field are Uber and Lyft. The main issue with these solutions is the cost. Students should be able to arrive at school at no cost. As a result, both of these services are inadequate as they will charge students a fee to arrive at their destination. Furthermore, in the scope of highschool carpooling, parents need to be involved to see their students' location for pickup. These two services once again do not account for this need. Finally, in the evenings, when students need to be picked up by another parent or need an estimated time of arrival for pickup, they will be unable to find such information via Uber or Lyft.

However, the main goal of our application is the same as Uber and Lyft: transporting a user from location A to B. In order to improve on this base idea, SharePool presents a few advantages.

- Being specifically aimed at the student population to enable easy carpooling
- Providing a parent view to understand where their child is
- Streamlining pickups in the evening for multiple parents by providing the locations of multiple students
- Utilizing a built-in calendar service that coordinates when students will be joining a carpool (i.e. student A cannot carpool on Monday because have programming team)

Architecture

<img src="https://firebasestorage.googleapis.com/v0/b/share-ff6c6.appspot.com/o/documentation%2FUntitled%20design%20(14).png?alt=media&token=d4dfcc1c-5424-41f0-813d-40902be3beb1" width="500">

# User Interface

More detailed overview: <a href="https://docs.google.com/presentation/d/1HZ7SRH_6nC0nRpSxr_j3cDCzgjDWCj1n96qr3oCYHMw/edit#slide=id.g21131501bb0_1_0">here</a>

This user interface enables the user to view account related details. Furthermore, the map is the primary view to focus the user's attention on the most critical portion of the application. They then have the option to create or join a new cluster, prompted when clicking on “clusters.” A plethora of settings can be found in the settings menu from the color theme of the app to changing the password. Sign-ins will require 2FA on the first sign in and then never after. 

The map view as well as the cluster tab simplifies the concept for the user in a friendly format for them to view. Additionally, the “plan trip” button will enable the user to start a new shared trip with the simple click of a button. Though the concepts involved in allowing for the app to function may be complex, the user is able to view a highly simplified and easy to use application.
Flow Chart / Systems Diagram

<img src="https://firebasestorage.googleapis.com/v0/b/share-ff6c6.appspot.com/o/documentation%2Fsystemsdiagram.png?alt=media&token=2b7226f5-f5d5-4eb3-ba46-92c7ee86eb3c">

# Persistent Storage
Our application stores associated data in a cloud database format because users need to be able to form clusters of carpoolers. We are highly considering Firebase based on the reliance of building with Flutter. Both Flutter and Firebase are made through Google, increasing the in-house support of related technologies. In order to fulfill the cluster storage requirement, we will utilize Firestore, which runs on document-based record storage.

<br> <i>Data: users collection, groups collection</i>

# Poster Presentation

<img src="https://firebasestorage.googleapis.com/v0/b/share-ff6c6.appspot.com/o/documentation%2Fposter%20draft%20afg.jpg?alt=media&token=458fca88-e9e4-416d-ada6-91ac1073eb9a" width="450">


# References

References

‘It’s cold and the bus passed me.’ How transportation problems fuel absenteeism in Detroit. (2023, March 22). Chalkbeat Detroit. https://detroit.chalkbeat.org/2023/3/22/23650149/detroit-students-transportation-bus-chronic-absenteeism-attendance

New York City Council holds hearing on issues with school bus transportation. (2022, November 21). ABC7 New York. https://abc7ny.com/nyc-bus-transportation-issues/12478329/

West, C. (2021, December 10). A surprising reason keeping students from finishing college: A lack of transportation. The Hechinger Report. https://hechingerreport.org/a-surprising-reason-keeping-students-from-finishing-college-a-lack-of-transportation/


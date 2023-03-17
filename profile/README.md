<p align="center">
<img src="https://firebasestorage.googleapis.com/v0/b/share-ff6c6.appspot.com/o/documentationAndLogos%2FSharePool%20(1).png?alt=media&token=e3f236b9-50bf-4471-859b-a96bc6a068a1" align="center" width="500">
</p>

# Statement of Goals

In the present, users looking to carpool are unable to find an outlet to allow them to plan with friends. Rather, they must pay a third party source to allow them to carpool otherwise. Furthermore, when planning a trip with friends, determining the optimal location of meeting may be problematic. Some locations may be ideal for parties; however, they may have traffic ridden roads making them inaccessible. This issue is especially prevalent for individuals attempting to carpool to school together. When multiple individuals carpool together, communication across the party tends to be lacking. 

Our goal is to create an application that solves these issues by <br>
(a) Aid those without cars to carpool with others in various settings (i.e. school or church groups)<br>
(b) Determine the optimal meeting location of the individual carpoolers given their initial locations and the one that they wish to visit.<br>
(c) Enable communication across a party to allow for greater connectivity

Note: Optimal location is defined by the location that requires the least amount of time total for the group to reach the end location.

# Functional Description (MVP)
Our application will store carpoolers in clusters with assigned drivers. These clusters then all are granted access to view the same map view and information. Chats within the group are then created to allow for communication. Authentication will occur through Firebase while storage will primarily occur through MongoDB.
The 3 core features of the product are: 
<br> 1) Real-time location tracking for all members of the carpool cluster
<br> 2) Communication within the cluster to enable connectivity
<br> 3) An algorithm to find the best route to utilize within the carpool cluster based on differing starting locations <br>
> 3a) Where route is the shortest route overall <br>
> 3b) Where the route is the shortest for person a, b, c… <br> 
> 3c) Where route requires equal driving from all people <br>
4) Technical and Data Feasibility

In order to accomplish the tracking features of the application, a few pieces of information will be required from clients:

- A mobile phone number
- Location tracking services via Google Maps API
- Client names
- Client age
- Client email

In order to create the desired cluster format, a noSQL framework will be used to optimize searching. A NoSQL database will require too long for searching records. Furthermore, the data must be stored in the cluster format. A preview of the cluster will be

	clusterName: cluster0
	users: [name, number], [name, number]. [name, number]
	mapsAPIToken: ZXYRXYJtyrfyjweOIL
	clusterSettingA: true
	clusterSettingB: false
	etc.

If a user decides to leave the carpool during an already planned trip, the algorithm will instantaneously update to account for the change. The algorithm will also be able to adjust for a change in final destination.

Rough API Design & Existing Technologies Integrations

<img src="https://firebasestorage.googleapis.com/v0/b/sharepool-e5a30.appspot.com/o/documentation%2FSharePool.png?alt=media&token=229b4fe0-eb63-4cb1-b5bd-8ed087c216dc">

# User Interface

More detailed overview: <a href="https://docs.google.com/presentation/d/1HZ7SRH_6nC0nRpSxr_j3cDCzgjDWCj1n96qr3oCYHMw/edit#slide=id.g21131501bb0_1_0">here</a>

This user interface enables the user to view account related details. Furthermore, the map is the primary view to focus the user's attention on the most critical portion of the application. They then have the option to create or join a new cluster, prompted when clicking on “clusters.” A plethora of settings can be found in the settings menu from the color theme of the app to changing the password. Sign-ins will require 2FA on the first sign in and then never after. 

The map view as well as the cluster tab simplifies the concept for the user in a friendly format for them to view. Additionally, the “plan trip” button will enable the user to start a new shared trip with the simple click of a button. Though the concepts involved in allowing for the app to function may be complex, the user is able to view a highly simplified and easy to use application.
Flow Chart / Systems Diagram

<img src="https://firebasestorage.googleapis.com/v0/b/sharepool-e5a30.appspot.com/o/documentation%2Fsystemsdiagram.png?alt=media&token=06d4620e-26f7-487a-8a4f-4b2ac2d37a59">

# Persistent Storage
Our application stores associated data in a cloud database format because users need to be able to form clusters of carpoolers. We are highly considering Firebase based on the reliance of building with Flutter. Both Flutter and Firebase are made through Google, increasing the in-house support of related technologies. In order to fulfill the cluster storage requirement, we will utilize Firestore, which runs on document-based record storage.

<br> <i>Data: users collection, groups collection</i>

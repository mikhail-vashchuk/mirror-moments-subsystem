# Objects

## Goal

The goal of this stage is to identify the main objects of the subsystem, describe their responsibilities, and define the relationships between them as a basis for further object-oriented modeling.

## Main objects

The main objects of the subsystem are **Person**, **LiveMoment**, and **JoinRequest**.

### Person
A person is the main participant of the subsystem. A person can open a moment, discover moments created by others, and request access to join them. Depending on the situation, a person may act in different roles, such as the host of a moment or a participant accepted into it.

### LiveMoment
A live moment is the central object of the subsystem. It represents an active real-time interaction space opened by one person within the Mirror platform. A live moment can be discovered by others and can receive join requests while it remains active.

### JoinRequest
A join request is an object that represents an attempt of one person to enter a moment opened by another person. It exists until the host reviews it and decides whether to accept or reject it.

## Object responsibilities

### Person
The responsibility of the **Person** object is to represent an individual participant of the subsystem. A person can open a live moment, discover moments created by others, send join requests, and participate in interaction after approval.

### LiveMoment
The responsibility of the **LiveMoment** object is to represent an active real-time interaction space. It stores the existence of a moment within the platform, allows others to discover it, and serves as the object to which join requests are addressed.

### JoinRequest
The responsibility of the **JoinRequest** object is to represent a controlled request for entering a live moment. It connects a person who wants to join with the moment they want to enter and remains active until it is accepted or rejected by the host.

## Relationships between objects

A **Person** can create a **LiveMoment**. In this case, the person becomes the host of that moment.

A **Person** can also discover a **LiveMoment** created by another person and send a **JoinRequest** to it.

A **JoinRequest** is associated with one **Person** who sends it and one **LiveMoment** to which it refers.

A **LiveMoment** can receive multiple join requests from different people while it remains active.

After approval, a person can take part in a live moment created by another person.

## Notes

At the current stage, the object model is limited to the basic mechanics of moment creation and joining. A live moment in Mirror is not intended to be treated as a generic video session. In future refinement of the project, additional attention may be given to the form, reason, or opening context of a moment, since this aspect may influence how a moment differs from a simple call or broadcast.

At this stage, the roles of **host** and **participant** are treated as contextual roles of the **Person** object rather than as separate main objects.
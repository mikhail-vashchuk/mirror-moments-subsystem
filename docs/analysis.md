# Analysis

## Topic

Subsystem for creating and joining live moments between people within Mirror.

## Goal

The goal of this work is to analyze the domain area of the subsystem for creating and joining live moments between people within the Mirror platform, and to define its main entities, interaction scenarios, boundaries, and requirements for further design and implementation in C++.

## Subject of development

The subject of development is a subsystem of the Mirror platform responsible for creating moments, discovering active ones, sending join requests, and managing access to real-time interaction between people.

## Domain area

The domain area of this subsystem is live video-based interaction between people within the Mirror platform. In the context of this project, video is considered the primary medium for sharing real-time moments, since it allows participants to perceive presence, reactions, and emotional nuances more directly than text-based or static forms of communication.

Within this environment, a person can open a moment, while others can discover it and request to join. Access is controlled by the person who opened it, which makes participation selective and intentional rather than open and uncontrolled. As a result, interaction is treated not as ordinary messaging or generic broadcasting, but as a shared real-time experience between people.

## Domain analysis

The subsystem is focused on moments that can be opened by one person and joined by others through controlled access. Its purpose is to support structured real-time interaction in which participation depends on the host’s decision.

The main participants are people acting in different roles. One person opens a moment and acts as its host. Others can discover available moments, request to join them, and become participants after approval.

The central entity of the subsystem is a live moment. It represents an active real-time interaction space between people. Another important entity is a join request, which appears when one person wants to enter a moment created by another person and remains active until it is accepted or rejected.

The main processes of the subsystem are creating a moment, discovering active moments, sending a join request, reviewing it, accepting or rejecting it, joining the interaction, and closing the moment.

The subsystem uses video as the main interaction format, which makes presence and real-time reactions more direct than in text-based communication. At the same time, the current analysis is limited to the basic mechanics of creating moments and joining them, without covering recommendation logic, ranking, reflection building, or extended profile representation.

The current analysis also does not cover the broader architectural mechanisms through which the Mirror platform is expected to leave a person with a sense of inner lightness, freedom of thought, and emotional relief after meaningful interaction. Although this effect is outside the scope of the present subsystem, it remains one of the main long-term design goals of the platform and one of the main reasons for its future architectural development.

## Existing approaches / analogs

Existing digital interaction systems include text messaging platforms, video call services, live streaming platforms, and room-based communication systems.

Text messaging platforms do not focus on visible real-time presence. Video call services support direct interaction, but they are usually private or invitation-based. Live streaming platforms are built around watching and reacting rather than joining a shared moment through host approval. Room-based systems support active communication, but they are not necessarily centered around a moment as a meaningful interaction unit.

In contrast, the subsystem proposed in this project is based on live video interaction, controlled access, and joining an active moment created by another person.

## Problem statement

The task of this work is to design a subsystem of the Mirror platform that allows people to create live moments, discover active ones, request access to them, and join them through controlled entry based on the host’s decision.

## Main system entities

### Person
A person is the main participant of the subsystem. A person can open a moment, discover moments created by others, request access to them, and take part in real-time interaction after approval.

### LiveMoment
A live moment is the central entity of the subsystem. It represents an active real-time interaction space opened by one person within the Mirror platform.

### JoinRequest
A join request is created when one person wants to enter a moment opened by another person. It is reviewed by the host and may be accepted or rejected.

### Participation
Participation represents the state in which a person has been accepted into a moment and becomes involved in the interaction.

## Main interaction scenarios

### Scenario 1: Creating a moment
A person opens a new moment within the platform. After creation, the moment becomes available for discovery by others.

### Scenario 2: Discovering active moments
A person browses available moments and selects one that appears relevant or interesting for possible participation.

### Scenario 3: Sending a join request
After choosing a moment, a person sends a join request to the host in order to gain access to the interaction.

### Scenario 4: Reviewing a join request
The host receives the request and reviews it. At this stage, the host decides whether to accept or reject the request.

### Scenario 5: Joining the interaction
If the request is accepted, the person becomes a participant and joins the active moment.

### Scenario 6: Closing a moment
After the interaction is completed, the host closes the moment, and it is no longer available for discovery or joining.

## Conclusion

The analysis of the subject domain made it possible to define the purpose, boundaries, and basic structure of the subsystem for creating and joining moments within the Mirror platform. The main participants, entities, processes, and constraints of the subsystem were identified, and its difference from related digital interaction approaches was outlined.

The obtained results form the basis for further object-oriented modeling of the subsystem, including the description of objects, classes, interactions, and state transitions, as well as for its later implementation in C++.

At the same time, this subsystem is considered only as one part of the broader Mirror concept. The larger goal of the platform is connected not only with technical interaction itself, but also with creating a space that can leave a person with a sense of inner lightness, freedom of thought, and emotional relief after meaningful contact with others.
# **Ralf - Software Requirements Specification**

## Table of contents

* [1 Introduction](#1-introduction)
  + [1.1 Purpose](#11-purpose)
  + [1.2 Scope](#12-scope)
* [2 Overall Description](#2-overall-description)
  + [2.1 Vision](#21-vision)
  + [2.2 Use Case Diagram](#22-use-case-diagram)
  + [2.3 Technology Stack](#23-technology-stack)
* [3. Specific Requirements](#3-specific-requirements)
  + [3.1 Functionality](#31-functionality)
  + [3.2 Usability](#32-usability)
  + [3.3 Reliability](#33-reliability)
  + [3.4 Performance](#34-performance)
    - [3.4.1 Response time](#341-response-time)
    - [4.4.2 Capacity and Storage](#442-capacity-and-storage)
  + [3.5 Supportability](#35-supportability)
  + [3.6 On-line User Documentation and Help System Requirements](#36-on-line-user-documentation-and-help-system-requirements)
  + [3.7 Purchased components](#37-purchased-components)
  + [3.8 Interfaces](#38-interfaces)
  + [3.8.1 User interfaces](#381-user-interfaces)
    - [3.8.2 Hardware interfaces](#382-hardware-interfaces)
    - [3.8.3 Software interfaces](#383-software-interfaces)
    - [3.9.4 Communication Interface](#394-communication-interface)

## 1 Introduction

### 1.1 Purpose

This Software Requirements Specification (SRS) fully describes all specifications for the application "RALF". It includes an overview about this project and its vision as well as information about it's functionalities and the boundaries of the development process.

### 1.2 Scope

This project will be created as an Web-Proxy

Users of our product are either Consumers or Administrators.

The features of this Product are:

- Account Management

Users can create accounts with which they can log in again at a later time. Administrators have an overview over all accounts and can edit permissions or delete users.

- Creating new Flows/Filterprofile

Users can create Flows. Flows are actions or rules that are applied to an ICS file that is provided by the user.

- Editing existing Flows

It is possible to manage existing flows by deleting or editing them. Editing includes a few options like change the Regex or changing filtered subjects.

- Collect information from .ics sources

User can enter a .ics source (e.g. by URL) and the program automatically collects needed data from the source.

- Provide .ics endpoints with a filtered output

The data from the .ics sort is filtered or changed with the used flow and then send back to a .ics endpoint e.g. Google Calender

- Health Checks

All connections to databases and services which do anything should be actively monitored. A health check is used to check, if the services are working and if connections are open.

## 2 Overall Description

### 2.1 Vision
Many students complain about the look and feel of our native school timetable. Inspired by this we want to change the way students interact with that data. It should be made easily accessible to change data and make the timetable individual and valuable for each student.

### 2.2 Use Case Diagram
![image.png](https://cdn.discordapp.com/attachments/1032247172562948197/1032257766615679037/Screenshot_2022-10-19_at_13.43.44.png)

### 2.3 Technology Stack
Backend: GoLang & MongoDB
Frontend: React
IDE: Jetbrains WebStorm & GoLand & VSCode & DataGrip
Project Management: Jetbrains Space
Deployment: Docker
Testing: Karate & Testify

## 3. Specific Requirements

### 3.1 Functionality
> **Note**: See [Functional Requirements](./functional-requirements).

### 3.2 Usability

- The user should intuitively know what to do and how to import data as well as change filters.

- We want to make sure the user can easily filter out or change things depending on how they see fit. 

- The user should also have a familiar feeling when using our app when compared to other apps

### 3.3 Reliability

- Our goal is to have the servers 99,9% of the time available. As our service delivers information that can be very important, we set a big focus on high availability.

- Because the service will be school and university related, we expect the rush hour to be in the morning time

- The accuracy is another metric where we leave no room for error, so we can allow no possibilities for wrong data

### 3.4 Performance

#### 3.4.1 Response time
 
- We will try to keep the response time to a minimum to ensure the user has a good and smooth performance

#### 4.4.2 Capacity and Storage

- Our infrastructure should be able to handle all incoming requests. It's also vital to be able to save all the user data such as passwords and emails. But our application doesn't require a lot of storage needs.


### 3.5 Supportability 

- Our application will be created with widely used technologies, this makes it more likely that these languages and frameworks will be supported for a longer time. 

- Our testing strategy also dictates to have a high test coverage to ensure the functionality of our application. It also helps to fix errors when adding or modifying code.


### 3.6 On-line User Documentation and Help System Requirements 

- Our design standards are supposed to be very intuitive so the user should not need a lot of help to navigate our site. We will implement a help button for people to help navigate the site for the first time.

### 3.7 Purchased components

- We purchased a domain for around 35€ a year. We can reuse a server we already have so we don't need to invest money on that.

### 3.8 Interfaces


### 3.8.1 User interfaces

- Sign In/Sign Up/Sign Out
- User Dashboard
- View filter profile
- Edit filter profile
- Create new filter profile
- Admin Dashboard
- Manage users

#### 3.8.2 Hardware interfaces

- Server
- Storage

#### 3.8.3 Software interfaces

- REST

#### 3.9.4 Communication Interface

- HTTPS

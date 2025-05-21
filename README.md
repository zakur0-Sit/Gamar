# Software Requirements Specification

## For GAMAR (Gaming Augmented Mixed-reality App Resource)

**Version:** 1.0  
**Authors:** [Cazacu Ion, Cucuteanu Lucian-Andrei, Dragoș Gabriel-Cătălin, Palici Roberto, ]  
**Date:** [22/05/2025]  

---

## Table of Contents

- [1. Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Document Conventions](#12-document-conventions)
  - [1.3 Intended Audience](#13-intended-audience)
  - [1.4 Product Scope](#14-product-scope)
- [2. Overall Description](#2-overall-description)
  - [2.1 Product Perspective](#21-product-perspective)
  - [2.2 Product Functions](#22-product-functions)
  - [2.3 User Classes and Characteristics](#23-user-classes-and-characteristics)
  - [2.4 Operating Environment](#24-operating-environment)
  - [2.5 Constraints](#25-constraints)
  - [2.6 Assumptions and Dependencies](#26-assumptions-and-dependencies)
- [3. External Interface Requirements](#3-external-interface-requirements)
  - [3.1 User Interfaces](#31-user-interfaces)
  - [3.2 Hardware Interfaces](#32-hardware-interfaces)
  - [3.3 Software Interfaces](#33-software-interfaces)
  - [3.4 Communications Interfaces](#34-communications-interfaces)
- [4. System Features](#4-system-features)
  - [4.1 Notifications and Alerts](#41-notifications-and-alerts)
  - [4.2 MR Stat Expansion](#42-mr-stat-expansion)
  - [4.3 Community News](#43-community-news)
- [5. Other Nonfunctional Requirements](#5-other-nonfunctional-requirements)
  - [5.1 Performance](#51-performance)
  - [5.2 Safety](#52-safety)
  - [5.3 Security](#53-security)
  - [5.4 Quality Attributes](#54-quality-attributes)
  - [5.5 Business Rules](#55-business-rules)
- [Appendix A: Glossary](#appendix-a-glossary)

---

## 1. Introduction

### 1.1 Purpose

Gamar is a dual-platform application (mobile + MR headset) tailored for teenagers who enjoy competitive games like Fortnite and Call of Duty. It displays stats, overlays, news, and rankings in real time.

### 1.2 Document Conventions

- Fonts:
  - Headings: **Oxanium SemiBold**
  - Body text: *Oswald Regular*
  - News: *Fustat SemiBold*
- Colors from Style Guide:
  - Background: `#000A34`
  - Wins: `#4CAF50`
  - Losses: `#FF5A5F`
  - Global Leaderboard: `#02DA29`
  - Regional Leaderboard: `#D4DF00`

### 1.3 Intended Audience

This document targets:
- Developers and Designers
- Testers and QA
- Stakeholders and Product Owners

This product targets:
- Teen gamers
- Content creators

### 1.4 Product Scope

Gamar is a gaming assistant tool that overlays stats and insights during gameplay. It extends into mixed reality (MR) for immersive visualization of data and rankings.


---

## 2. Overall Description

### 2.1 Product Perspective

Gamar is an independent mobile + MR platform that integrates game data via APIs. It enhances gameplay by displaying stats in real time and visualizing them spatially via MR.

### 2.2 Product Functions

- **Overlay HUD**: Shows match data, team stats, win/loss summary.
- **News Feed**: Curated gaming news, community updates.
- **Leaderboards**: Color-coded (regional & global) rankings.
- **MR Display**: Immersive stat visualizations around the user.

### 2.3 User Classes and Characteristics

| User Class        | Description                                  |
|-------------------|----------------------------------------------|
| Casual Gamers     | Use overlays occasionally for tracking       |
| Competitive Players | Rely on stats for performance optimization |
| Creators          | Use visuals for stream content               |

### 2.4 Operating Environment

- **Mobile App**: Android 11+, iOS 15+
- **Headset App**: Meta Quest, Apple Vision Pro
- Backend via Node.js and WebSocket API

### 2.5 Constraints

- Dependent on availability and limits of external game APIs
- MR requires optimized rendering and battery efficiency

### 2.6 Assumptions and Dependencies

- Stable internet connection
- Overlay and MR permissions are granted
- Game data is retrievable in real time

---

## 3. External Interface Requirements

### 3.1 User Interfaces

- **Design Language**: Flat icons, slight rounded corners (5px)
- **Icons**: 22x22px standard, 27x27px key indicators
- **UI Colors**:
  - Selected icons: `#2DD881`
  - Menu icons: `#05B2DC`
  - Text: `#FFFFFF`

### 3.2 Hardware Interfaces

- Mobile devices with overlay capabilities  
- MR headset

### 3.3 Software Interfaces

- Game platform APIs (Epic Games, Activision)
- OAuth2 authentication
- MongoDB/SQL for data storage

### 3.4 Communications Interfaces

- HTTPS for secure connections
- WebSocket for real-time data streaming

---

## 4. System Features

### 4.1 Notifications and Alerts

- Game wins (`#4CAF50`) and losses (`#FF5A5F`)  
- Event pop-ups: updates, patches, community tournaments  
- MR environment: voice or gesture-triggered alerts

### 4.2 MR Stat Expansion

- Stats and game data visualized spatially via MR headset  
- Interactions via gaze or controller  
- Can rotate, zoom, and pin data in virtual space

### 4.3 Community News

- Aggregated from gaming news sources  
- Displayed with *Fustat* font for emphasis  
- Includes filters by game title or topic

---

## 5. Other Nonfunctional Requirements

### 5.1 Performance

- Overlay should load in under 1 second  
- Must handle 10,000 concurrent users  

### 5.2 Safety

- UI must avoid obstructing important game elements  
- MR safety boundary warnings and onboarding calibration  

### 5.3 Security

- Encrypted data storage  
- OAuth2 login  
- Secure WebSocket and HTTPS communications  

### 5.4 Quality Attributes

- **Usability**: Clean UI, intuitive icons  
- **Scalability**: Cloud-native, supports load scaling  
- **Reliability**: 99% uptime requirement  

### 5.5 Business Rules

- Parental control options required  
- Data anonymized for analytics

---

## Appendix A: Glossary

- **GAMAR**: Gaming Augmented Mixed-reality App Resource  
- **HUD**: Heads-Up Display  
- **MR**: Mixed Reality  
- **WebSocket**: Protocol for real-time two-way communication  
- **COPPA**: Children's Online Privacy Protection Act  

---

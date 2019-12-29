---
title: SOLID Principles
date: "2019-12-28"
description: "SOLID Principles"
---


Today I was going through the solid principles training. I had understood key concepts of UML notation and SOLID principles.

# UML Diagrams

## Inheritance 

This is "IS A " relationship. For example Swift is a Bird. This is indicated by a lollypop symbol. 

## Assosiation
This is a bidirectional relationship. This is indicated by a straight line.

## Aggregation
This is HAS A relation . If you take A and B classes. A class can exist without other class, but B will be having A.

## COMPOSITION
This is a tight coupled HAS A relationship.

# SRP
Single Responsibity of a class means the class has a single reason to change. 
Observer pattern with MVC  single responsibility principle.

# Interface segregation principle
Once lot of clients depend on the component, the changes for a client in the component would start effecting other clients. This is the violation of SRP. 
To counter this , this principle says to have multiple interfaces implemented, and the component subdivided to smaller components.

# Liskov substitution principle
Runtime substituion of any interface should behave simlarly.

## Inheritance vs Composition
Inheritance is the tightest coupling. Use it one or two levels. Use composition instead.

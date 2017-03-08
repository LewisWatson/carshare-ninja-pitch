#HSLIDE

# carshare.ninja

#HSLIDE

## What is carshare.ninja

- Tracks of who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Driven by a flexible and fair scoring algorithm<!-- .element: class="fragment" data-fragment-index="3" -->
- Accessible via Progressive Web Application <!-- .element: class="fragment" data-fragment-index="4" -->
  - Reliable - loads instantly even with unreliable network
  - Fast - won't leave you hanging, you've got somewhere to go!
  - Engaging - feels like a native app

#VSLIDE

## Member Scoring System

`$$Score = \frac{DistanceAsPassenger}{DistanceAsDriver}$$`

Members with the lowest score should drive next <!-- .element: class="fragment" data-fragment-index="2" -->

#VSLIDE

Ranking members by the benefit they personally recieve keeps things simple and fair.

#VSLIDE

The scoring system also flexible and can handle

- holidays <!-- .element: class="fragment" data-fragment-index="1" -->
- sick days <!-- .element: class="fragment" data-fragment-index="2" -->
- differing shift patterns <!-- .element: class="fragment" data-fragment-index="3" -->
- differing distances. Maybe you pick a member up on the way? <!-- .element: class="fragment" data-fragment-index="4" -->

#HSLIDE

# Technical Overview

#VSLIDE

![Architecture Overview](assets/overview.png)

#VSLIDE

## API

- Stateless microservice written Go  <!-- .element: class="fragment" data-fragment-index="1" -->
- To be deployed as an autoscaling service in Kubernetes <!-- .element: class="fragment" data-fragment-index="2" -->
- Authentication via Firebase JWT tokens <!-- .element: class="fragment" data-fragment-index="3" -->
  - I created library for this: [firebase-jwt-auth](https://github.com/LewisWatson/firebase-jwt-auth) <!-- .element: class="fragment" data-fragment-index="4" -->
- Scalable data persistance via MongoDB <!-- .element: class="fragment" data-fragment-index="5" -->

#VSLIDE

## Front End

- Written in Angular2  <!-- .element: class="fragment" data-fragment-index="1" -->
- Material design <!-- .element: class="fragment" data-fragment-index="2" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="3" -->
  - Open Web <!-- .element: class="fragment" data-fragment-index="3" -->
  - Service workers <!-- .element: class="fragment" data-fragment-index="3" -->
  - Offline first <!-- .element: class="fragment" data-fragment-index="3" -->
- Firebase authentication <!-- .element: class="fragment" data-fragment-index="4" -->
  - JWT token included with every API call <!-- .element: class="fragment" data-fragment-index="4" -->

#HSLIDE

# Current State

#VSLIDE

## Front End

- Implemented some of the key views
- Supports Firebase anonymouse authentication. 
  - More providers to come
  - JWT included in every API call
- PWA mostly implemented, still need to tackle offline first

#VSLIDE

#HSLIDE

## One More Thing...

#VSLIDE

## Early preview of Progressive Web App available at

### [https://carshare.ninja](https://carshare.ninja)

#HSLIDE

FIN

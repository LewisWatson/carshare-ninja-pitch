#HSLIDE

# carshare.ninja

#HSLIDE

## What is carshare.ninja

- Tracks of who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Driven by a flexible and fair scoring algorithm <!-- .element: class="fragment" data-fragment-index="3" -->
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

## API

- Stateless microservice written Go  <!-- .element: class="fragment" data-fragment-index="1" -->
- To be deployed as an autoscaling service in Kubernetes <!-- .element: class="fragment" data-fragment-index="2" -->
- Authentication via Firebase JWT tokens <!-- .element: class="fragment" data-fragment-index="3" -->
  - I created library for this called [firebase-jwt-auth](https://github.com/LewisWatson/firebase-jwt-auth)
- RESTful and conforms to JSON:API specifications <!-- .element: class="fragment" data-fragment-index="5" -->
- Scalable data persistance via MongoDB <!-- .element: class="fragment" data-fragment-index="6" -->

#VSLIDE

## Front End

- Written in Angular2  <!-- .element: class="fragment" data-fragment-index="1" -->
- Material design <!-- .element: class="fragment" data-fragment-index="2" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="3" -->
  - Open Web
  - Service workers
  - Offline first
- Firebase authentication <!-- .element: class="fragment" data-fragment-index="4" -->
  - Username/Password, social, anonymous 
  - JWT token included with every API call

#VSLIDE

![Architecture Overview](assets/overview.png)

#HSLIDE

# Current State

#VSLIDE

## Front End

- Implemented some of the key screens
  - Still need to implement the full set
- Firebase anonymous authentication.
  - More providers to come
  - JWT included in every API call
- PWA features mostly implemented, still need to tackle offline first
- Hosted on Firebase.
- HTTPS certificate provided by LetsEncrypt

#VSLIDE

## API

- Supports most required actions
- Integrates with MongoDB
- Docker image available on dockerhub
- Able to verify Firebase JWT Tokens
- Currently restricting access based on JWT
- Need to figure out where to host it

#HSLIDE

## One More Thing...

#VSLIDE

#### Early Preview of Progressive Web App available at

[https://carshare.ninja](https://carshare.ninja)

#HSLIDE

FIN

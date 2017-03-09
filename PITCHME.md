#HSLIDE

# Car Share Ninja

#HSLIDE

## What is Car Share Ninja?

- Tracks of who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Driven by a flexible and fair scoring algorithm <!-- .element: class="fragment" data-fragment-index="3" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="4" -->
  - Reliable - loads instantly even with unreliable network
  - Fast - won't leave you hanging, you and your buddies have somewhere to go!
  - Engaging - feels like a natural app on device

#VSLIDE

## Member Scoring System

`$$Score = \frac{DistanceAsPassenger}{DistanceAsDriver}$$`

Members with the lowest score should drive next <!-- .element: class="fragment" data-fragment-index="2" -->

#VSLIDE

Ranking members by the benefit they personally recieve keeps things simple and fair.

#VSLIDE

Offers great flexibility.

Can handle: <!-- .element: class="fragment" data-fragment-index="1" -->

- holidays <!-- .element: class="fragment" data-fragment-index="1" -->
- sick days <!-- .element: class="fragment" data-fragment-index="1" -->
- differing shift patterns <!-- .element: class="fragment" data-fragment-index="1" -->
- differing distances, maybe you pick a member up on the way? <!-- .element: class="fragment" data-fragment-index="1" -->

#HSLIDE

# Technical Overview

#VSLIDE

## API

- Stateless microservice written Go  <!-- .element: class="fragment" data-fragment-index="1" -->
- To be deployed as an autoscaling service in Kubernetes <!-- .element: class="fragment" data-fragment-index="2" -->
- Firebase JWT Authentication <!-- .element: class="fragment" data-fragment-index="3" -->
  - I created library for this called [firebase-jwt-auth](https://github.com/LewisWatson/firebase-jwt-auth)
- RESTful and implements JSON:API <!-- .element: class="fragment" data-fragment-index="4" -->
- MongoDB data store <!-- .element: class="fragment" data-fragment-index="5" -->

#VSLIDE

## Front End

- Written in Angular2  <!-- .element: class="fragment" data-fragment-index="1" -->
- Material design <!-- .element: class="fragment" data-fragment-index="2" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="3" -->
  - Benefit from the reach of the web <!-- .element: class="fragment" data-fragment-index="4" -->
  - Service workers acting as client side proxy <!-- .element: class="fragment" data-fragment-index="5" -->
    - Cache key resources to improve responsivenes
    - App takes responsibility for what happens if there is no network
  - Will earn it's place on users home screen, along side native apps <!-- .element: class="fragment" data-fragment-index="6" -->
- Firebase authentication <!-- .element: class="fragment" data-fragment-index="7" -->
  - Username/Password, social, anonymous 
  - JWT token included with every API call

#HSLIDE

# Current State

#VSLIDE

## API

- Majority of REST endpoints implemented
- Integrates with MongoDB
- Docker image
- Firebase JWT support
- `//TODO` <!-- .element: class="fragment" data-fragment-index="1" -->
  - Restrict access based on user
  - Need to figure out where to host it

#VSLIDE

## Front End

- Implemented some basic screens
- Firebase anonymous authentication.
  - JWT included in every API call
- PWA features mostly implemented
- Hosted on Firebase.
- LetsEncrypt HTTPS certificate
- `//TODO` <!-- .element: class="fragment" data-fragment-index="1" -->
  - Finish implementing UI
  - Add more authentication providers
  - Cache API data to fully implement Offline First

#HSLIDE

## One More Thing...

#VSLIDE

#### Early Preview Available

[https://carshare.ninja](https://carshare.ninja)

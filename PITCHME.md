---

# Car Share Ninja

---

## What is Car Share Ninja?

- Tracks who does what in a car share <!-- .element: class="fragment" data-fragment-index="1" -->
- Suggests who should drive next <!-- .element: class="fragment" data-fragment-index="2" -->
- Driven by a flexible and fair scoring algorithm <!-- .element: class="fragment" data-fragment-index="3" -->
- Progressive Web Application <!-- .element: class="fragment" data-fragment-index="4" -->
  - Reliable - loads instantly even with unreliable network
  - Fast - won't leave you hanging, you and your buddies have somewhere to go!
  - Engaging - feels like a natural app on device

---

## Member Scoring System

`$$Score = \frac{DistanceAsPassenger}{DistanceAsDriver}$$`

Members with the highest score should drive next <!-- .element: class="fragment" data-fragment-index="2" -->

---

Ranking members by the benefit they personally recieve keeps things simple and fair.

---

## Flexibility

Can handle: <!-- .element: class="fragment" data-fragment-index="1" -->

- holidays <!-- .element: class="fragment" data-fragment-index="1" -->
- sick days <!-- .element: class="fragment" data-fragment-index="1" -->
- differing shift patterns <!-- .element: class="fragment" data-fragment-index="1" -->
- differing distances, maybe you pick a member up on the way? <!-- .element: class="fragment" data-fragment-index="1" -->

# Technical Overview

---

## API

- Stateless microservice written [Go](https://golang.org)  <!-- .element: class="fragment" data-fragment-index="1" -->
- To be deployed as an autoscaling service in [Kubernetes](https://kubernetes.io/) <!-- .element: class="fragment" data-fragment-index="2" -->
- [Firebase JWT Authentication](https://firebase.google.com/docs/auth/admin/verify-id-tokens#verify_id_tokens_using_a_third-party_jwt_library) <!-- .element: class="fragment" data-fragment-index="3" -->
  - Currently no official library, so created one called [firebase-jwt-auth](https://github.com/LewisWatson/firebase-jwt-auth)
- RESTful and implements [JSON:API](http://jsonapi.org/) <!-- .element: class="fragment" data-fragment-index="4" -->
- [MongoDB](https://www.mongodb.com/) data store <!-- .element: class="fragment" data-fragment-index="5" -->

---

## Front End

- [Progressive Web Application](https://developers.google.com/web/progressive-web-apps/) written in [Angular2](https://angular.io/)  <!-- .element: class="fragment" data-fragment-index="1" -->
- Uses [Material design](https://material.io/guidelines/material-design/introduction.html)<!-- .element: class="fragment" data-fragment-index="2" -->
- [Firebase authentication](https://firebase.google.com/docs/auth/) <!-- .element: class="fragment" data-fragment-index="7" -->
  - Uses official Angular2 library [AngularFire2](https://github.com/angular/angularfire2)
  - Username/Password, social, and anonymous
  - [JWT](https://jwt.io) token included with every API call

---

#### Early Preview Available

[https://carshare.ninja](https://carshare.ninja)

##### Source

https://github.com/LewisWatson/carshare-angular2/
https://github.com/LewisWatson/carshare-back/
http://gopkg.in/LewisWatson/firebase-jwt-auth.v1
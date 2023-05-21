# Food-Delivery-System-Design-Practice
Practicing system design principle and etc. I will be focusing on food delivery system which is very challenging desing. There are a lot of aspects to concern.

# Functional requirements
- As a user, I should be able to search available restaurants nearyby me.
- As a user, I should be able to ordering foods via restaurant.
- As a rider, I should be able to search requesting orders nearby me.
- As a business owner, I should be able to

# Addendum
- number of users 10,000,000
- number of riders 5,000,000
- number of restaurants 1,000,000
- approximate daily active users 100,000 ~ 200,0000
- approximate daily active riders 50,000 ~ 100,0000
- approximate daily active restaurants 500,000 ~ 600,000

# System design

### Database design
I will be using NoSQL database because it's easy to scale horizontally and data structure is flexible.
Let's say we have four tables User, Rider, Restaurant, Order. I would have roughly design the tables as this.
[images]

### Challenge 
- One challenging problem is that, a user orders foods everyday so the Order table would get larger and larger which results in slower query. There are a lot of techniques to optimize the query response time, one of them is Sharding which I'm going to use. Sharding the Order table helps reducing the query response time so it's much more faster. I will select date as a sharding key which means that a new shard is created everyday.
- Finding nearby restaurants, The simpliest way to tell whether a restaraunt is nearby or not is by calculating the lattitude and longtitude but since we have large number of restaurants by doing that it would take a lot of resources to compute nearby restaurant. One of the techniques that I'm goint to use is Geohash. 
- Finding nearby riders, finding nearby riders is a little bit tricky because usually restaurant location isn't changed while riders are moving around.

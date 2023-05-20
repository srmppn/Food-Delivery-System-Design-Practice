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

### Schema design
I will be using NoSQL database because it's easy to scale horizontally and data structure is flexible.
Let's say we have four tables User, Rider, Restaurant, Order. I would have roughly design the tables as this.

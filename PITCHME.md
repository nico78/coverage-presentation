## The Dangers of Optimising for Coverage
### It's just one metric

---
### Tips!

- Press `F` to go fullscreen!

---?image=assets/warning-opinions-ahead.png

Note:

Bit of a rant which might seem like a straw man argument, some of it obvious but it led me to think about things which I hope are enlightening



---?image=assets/callbackHell.jpg


Note:
Some years back as a junior java developer  I was given a mandate -let's try this junit thing and try to get some components under test
Junit - elaborate haywire java mvc webframework login panel, callbacks, null checks all over the place, presentation logic mixed with business logic




---?image=assets/flossing.jpg

Note:
Testing - don't do it much, dimly aware that something I should be doing. like flossing. and important to be thorough.


---?image=assets/nullChecks.jpg

Note:
Some were hard - i couldn't make the thing null in some cases so lines weren't going to be executed. How was I supposed to mock the values returned from a static singleton? what about all this spring? Library called Power mock


---?image=assets/mazePuzzle.jpg

Note:

Blindly trying to tip the ball of green down every path like puzzle IMAGE


---

![Video](https://www.youtube.com/watch?v=saCaZ3KvYgY)

---?image=assets/rabbitHole.jpg

Note:

Ending up down a rabbit hole

---
##What was I really testing?


- it does what it currently does.  |
- In the way that it does it now.  |
- you'd better not touch anything now or the test will fail. |
- Every line of coverage is weighted equally |

---
## What does coverage actually tell us?

- Coverage tracks which lines of code are *executed* by tests.


Note:

you can write a happy path test which does no assertions and still get high coverage

Even with branch coverage (which tells you if you took both paths of an "if" statement). you still won't know if you've covered all possibilities - what if x is zero? or if x == y and it's not in an if statement. do you care?

Attempts to improve this -

---
### Mutation coverage - messes with a line of code

```scala
]​):
```

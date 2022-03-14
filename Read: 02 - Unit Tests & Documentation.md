## Unit Testing
-  Unit tests isolate and exercise specific units of your code, you can create a unit test by writing something that tests a method is isolation.

## General Notes on Unit Testing
- When we want to create a unit test we must add a project under the name of "Unit Test Project Template” after selecting “Test.”
- We arrange everything we need to run the experiment. With the arranging in place, we act, all of the arranging leads up to it, and everything afterward amounts to retrospection.Finally, we assert.  The invocation of the Assert class probably gave that one away.  But the assert concept in the unit test represents a general category of action that you cannot omit and have a unit test.  It asserts the hypothesis itself.  Asserting something represents the essence of testing.
- You should try to create one assert per test method.  Each test forms a hypothesis and asserts it, no test should ever contain a number of assertions other than one.
- Each test should handle its own setup.  The test runner will execute your stuff in whatever order it pleases. Avoid this interdependence.
- Resist the impulse to abstract test setup to other classes, and especially resist the impulse to abstract it into a base class.

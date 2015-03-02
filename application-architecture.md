# Application Architecture
The following categories are loose generalizations that cover 99% of front end
application code. It is helpful to separate the concerns of your code into these
categories to facilitate maintainability, testing, readability, and the
avoidance of bugs.

## Presentation / Interaction Layer

### Overview
The Presentation / Interaction Layer is the set of objects and functions that
define and control the appearance and behavior of your application's user
interface. **The responsibility of the presentation layer is to present the domain
and application state to the user.**

Presentation concerns include:
- What elements are containers for dynamic content?
- How will dynamic content be displayed? Through direct manipulation of an
  element's text content? Through the rendering of templates?
- What user interactions are defined for your application? What DOM events need
  to be registered for these interactions?

### How to Plan
Wireframes

## Domain / Data Layer
### Overview
Domain modeling is an approach to designing a system as a set of objects that
collaborate to accomplish the jobs to be done by the system.

- It provides a ubiquitous language, making it easier to reason about and
  communicate about the application.
- It reduces ambiguity by making you think and speak clearly about what the
  problem actually is.
- It makes both the problem and the solution more apparent by clarifying the
  problem domain
- It is made up of both real world and abstract objects.

#### Example
In a turn based game, you might have the following domain model:

##### Character

###### Responsibilities
- health
- attacks
- attack()

###### Collaborators
- has many Attacks
- belongs to a Game

##### Attack

###### Responsibilities
- minDamage
- maxDamage
- roll()

###### Collaborators
- belongs to a Character

##### Game

###### Responsibilities
- hero
- villain
- outcome

###### Collaborators
- has two characters

### How to Plan
Use CRC cards to plan the domain model.

## Application State Layer

### Overview
The application state is the set of variable and objects that represent the
state of your application at any given moment in time. For example, what
"screen" the user is on, what interactions the user has initiated, etc. The
application state is often implicit, which is difficult to reason about. It is
more conducive to plan the application states explicitly.

### How to Plan
It is helpful to wireframe all the application states first, then create URLs to
represent those states.

### Example
The following states represent our simple turn based game

- Start Screen (/)
- Character Selection Screen with no selection (/select/)
- Character Selection Screen with a selection (/select/finn)
- Game Play Screen (/play/finn/ice-king)
- Game Over Screen, won (/game-over/won)
- Game Over Screen, lost (/game-over/lost)

## Setup / Glue Code
The other code that doesn't fit into the other three categories. In many
applications, the entirety of the glue code will be:

```js
$(document).read(function(){
  window.router = new MyRouter();
  Backbone.history.start();
});
```

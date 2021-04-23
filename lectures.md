## 53. Purpose of Interfaces
- We know that:
  - Every value has a type;
  - Every function has to specify the type of its arguments
- So does that mean?
  - Every function we ever write has to be rewritten to accomodate different types even if the logic in it is identical?

## 54. Problems without interfaces
- In a function receiver, if we won't use the parameter we specify, we can just put the type of the parameter:

        $ func (englishBot) getGreeting() string {
        $   // some code here
        $ }

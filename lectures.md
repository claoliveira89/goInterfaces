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

## 55. Interfaces in Practice
- We use interfaces to define a method set or a function set; what different functions and return types it should have.

## 56. Rules of Interfaces

        type interfaceName interface {
            functionName(list of argument types) (list of return types)
        }

- Example:

        type bot interface {
            getGreeting(string, int) (string, error)
        }

- Concrete Type vs Interface Type
    - concrete type: something that we can create a value out of it, and access it, change it, etc... Such as map, struct, int, string, englishBot, deck...
    - interface type: we cannot create a value of interface type.

## Extra Interface Notes
- Interfaces are not generic types. Other languages have 'generic' types - go (famously) does not.
- Interfaces are 'implicit': we don't manually have to say that our custom type satisfies some interface.
- Interfaces are a contract to help us manage types. GARBAGE IN -> GARBAGE OUT. If our custom type's implementation of a function is broken then interfaces won't help us!
- Interfaces are tough. Step #1 is understanding how to read them. Understand how to read interfaces in the standard lib. Wrinting your own interfaces is tough and requires experience.     
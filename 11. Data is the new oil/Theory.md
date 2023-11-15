### What is HOC in react?

HOC are functions which take in a component and return a component. It takes in an existing component , tweaks/enhances it a little and returns the same component back.

`Why do we use it?`

- reusability
- predictable - HOC are pure functions - the enhanced components are never changed directly

`Example`
In swiggy.com , there are some promoted restaurants - so we have a restaurant card - we can just add the promoted label to the cards that want it. So we can develop a HOC which will take our exiting restaurant card as a input and return the card with label.

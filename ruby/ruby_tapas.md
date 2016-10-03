- use `fetch` with a block to provide defaults (instead of `||`) to allow `nil` or `false` to be explicitly passed as a key
  - using `||` will treat `nil`, `false`, and a completely missing key all the same and result in the same default value
- if your class has no state you don't need a class -- use a singleton object or module instead
  - classes in ruby are for sharing behaviour and containing state (e.g. ensuring correct initialization, acting as an object factory)
    - if a class is not performing both of those roles, you don't need a class
- use `&nil` as a second argument to `super` to ensure a block cannot inadvertendly be passed up the chain to a parent class
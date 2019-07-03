### Clean Code Summary

#### Naming

- use intention revealing names: `raduis` instead of `r`
- don't use abbreviations
- `name` is better than `nameString` (unnecessary informations)
- clear distinctions: avoid `getAcount`, `getAccounts`, `getAccountInfo` in the same class or e.g avoid `get`, `fetch`, `retrieve`
- use pronouncable and meaningful names
- searchable names ( can be found easily by search tools as per their meaning)
- avoid encodings (coded names)
- minimize the usage of prefixes like `addr_name`
- classes and objects should have noun or noun phrase names like `Customer`, `Account`
- methods should have verb or verb phrase name like `postPayment`, `deletePage`
- don't use cute or humorous or witty names
- accessors, mutators, and predicates should be named for their value and prefixed with `get`, `set`, and `is`.
- use names related to the solution applied like the pattern used e.g. factory , builder.
- if not possible relate it to the problem being solved, like relate variables to address e.g. `addressName`, `addressNumber` etc.
- add meaningful context, like creating a class which will hold the variables that are being used in the same context, this will make the variables belong to that class and thus have contextual meaning.

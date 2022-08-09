# Independence 

Let us expand the full joint distribution with a fourth variable: 

**P**(Toothache, Catch, Cavity, Weather) 

Now there are 2 * 2 * 2 * 4 = 32 entries. 

To work out questions such as: 

- How is the value of P(Toothache, Catch, Cavity Cloud) related to P(Toothache, Catch, Cavity)

We can use the product rule: 

P(Toothache, Catch, Cavity, Cloud) = 
  P(Cloud | Toothache, Catch, Cavity)P(Toothache, Catch, Cavity)

Given that clouds shouldn't affect the chances of any dental issue it is a reasonable assertion: 

P(Cloud | Toothache, Cavity, Catch) = P(Cloud)

The probability of a cloud occuring given that an individual has a Toothache, Cavity, and a dentist will use a Catch is the same probability as a Cloud occuring generally. 

This deduces: 

P(Toothache, Catch, Cavity, Cloud) = P(Cloud) * P(Toothache, Catch, Cavity)

This is an example of factoring 1 large joint distrubbution into smaller distributions using absolute independence. 

Weather and Dental Problems are independent 

Independence between propositions a and bb can be written like this: 

- P(a | b) = P(a)
- P(b | a) = P(b)
- P(a ^ b) = P(a)P(b)

Independence Assertions are usually based on some form of domain knowledge. 

It is used to dramatically reduce the amount of information necessary to specify a **full joint distribution** as the data can bbe factored into separate distributions on those subsets. 

Independence assertions help reduce the size of the domain representation and the complexity of the inference problem. 



## Definitions 

- **Independence** 
  - Independence is the decomposition of a large Joint distrubution by establishing/ deducing subsets of the data that have no affect on the probability of other subsets. 


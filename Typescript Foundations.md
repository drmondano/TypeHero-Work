Primitive Data Types Module
```
const playSong = (artistName: string, year: number) => {
  return `${artistName} was released in the year ${year}`;
};

const artistName: string = 'Frank Zappa';

const age:number = 52;

interface Musician {
  artistName: string;
  age: number;
  deceased: boolean;
  // add the rest
}

const musicianInfo = ({ artistName, age, deceased }: Musician) => {
  return `${artistName}, age ${age}${deceased ? ' (deceased)' : ''}`;
};

musicianInfo({
  artistName,
  age,
  deceased: true,
});
```
Type Aliases Module
```
// We completed the first alias (`Name`) for you to see as an example
type Name = string;

// Now try replacing `unknown` with a primitive data type that might be appropriate for `Year`
type Year = number;

type IsOperational = boolean;

type Count = number;

type Kilograms = number;

type Payload = {
  name: Name;
  mass: Kilograms;
  // the tests show that you need a `mass` property here
  // but first you might need to create an alias for `Kilograms`
  // because that's the value of `mass`
};
```
Literal Types Module
```

```

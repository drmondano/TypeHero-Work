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
type LiteralString = 'chocolate chips';
type LiteralTrue = true;
type LiteralNumbers = 1 | 2 | 3 | 4 | 5 | 6;
type LiteralObject = {
    name: 'chocolate chips',
    inStock: true,
    kilograms: 5,
  };
type LiteralFunction = (a: number, b: number) => number;

const literalString = 'Ziltoid the Omniscient';
const literalTrue = true;
const literalNumber = Math.random() > 0.5 ? 1 : 2;
const almostPi = 3.14159265358979323846264338327950288419716939937510582097494459230781640628620899862803482534211706798214808651328230664709384460955058223172535940812848111745028410270193852110555964462294895493038196442881097566593344612847564823378678316527120190914564856692346034861045432664821339360726024914127372458700660631558817488152092096282925409171536436789259036001133053054882046652138414695194151160943305727036575959195309218611738193261179310511854807446237996274956735188575272489122793818301194912983367336244065664308602139494639522473719070217986094370277053921717629317675238467481846766940513200056812714526356082778577134275778960917363717872146844090122495343014654958537105079227968925892354201995611212902196086403441815981362977477130996051870721134999999837297804995105973173281609631859502445945534690830264252230825334468503526193118817101000313783875288658753320838142061717766914730359825349042875546873115956286388235378759375195778185778053217122680661300192787661119590921642019891337;

const literalObject = {
    origin: 'asd',
    command: 'asd',
    item: 'asd',
    time: 'asd'
  };
type StringOrNumber = string | number ;
const literalFunction = (a: number, b: string) => {
	return b? a + b: a;
};
```
Index Signatures Module
```
type GroceryList = {
	[key:string]: number;
};

type InappropriateActionBySituation = {
	[key:string]: string[];
};

type CharactersById = {
  [key: number]: {
    id: number;
    name: string;
    status: string;
    species: string;
  };
};
```
The 'typeof' Operator Module
```
type Width = typeof width;
type Margin = typeof margin;
type Data = typeof d3ChartConfig.data;
type YScale = typeof d3ChartConfig.yScale;

type D3ChartConfig = typeof d3ChartConfig;
```
Indexed Types Module
```
type TheCoolestCarEverMade = Cars[4];
type TruckDriverBonusGiver = Donations['Taylor Swift'];
```
The 'keyof' operator Module
```

```

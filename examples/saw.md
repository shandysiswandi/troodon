## Simple Additive Weighting(SAW) Algorithm Examples

choose the one you like

```typescript
import { SAW, AttributeSaw } from "https://deno.land/x/troodon/mod.ts"; // Official Third Party Modules
// OR
import { SAW, AttributeSaw } from "https://denoland.id/x/troodon/mod.ts"; // Indonesia Third Party Modules
```

[Problems example 1](https://aeroyid.wordpress.com/2014/01/16/metodesimple-additive-weighting-saw/)

```typescript
const alternatives = ["Indra", "Roni", "Putri", "Dani", "Ratna", "Mira"];

const criterias = [
  [70, 50, 80, 60],
  [50, 60, 82, 70],
  [85, 55, 80, 75],
  [82, 70, 65, 85],
  [75, 75, 85, 74],
  [62, 50, 75, 80],
];

const weights = [35, 25, 25, 15];

const attributes = [
  AttributeSaw.BENEFIT,
  AttributeSaw.BENEFIT,
  AttributeSaw.BENEFIT,
  AttributeSaw.BENEFIT,
];

const example = new SAW(alternatives, criterias, weights, attributes);
console.log(example.result());
```

[Problems example 2](https://informasi-anakutm.blogspot.com/2016/06/cara-perhitungan-dan-contoh-kasus.html)

```typescript
const alternatives2 = ["A1", "A2", "A3", "A4"];

const criterias2 = [
  [150, 15, 2, 2, 3],
  [500, 200, 2, 3, 2],
  [200, 10, 3, 1, 3],
  [350, 100, 3, 1, 2],
];

const weights2 = [25, 15, 30, 25, 5];

const attributes2 = [
  AttributeSaw.COST,
  AttributeSaw.BENEFIT,
  AttributeSaw.BENEFIT,
  AttributeSaw.COST,
  AttributeSaw.BENEFIT,
];

const example2 = new SAW(alternatives2, criterias2, weights2, attributes2);
console.log(example2.result());
```
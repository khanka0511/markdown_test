# MathVec
Math library built with Typescript 🧮

Typescript tool for implementing math equations for your app

## Setup
- Clone repository `git clone https://github.com/zolbooo/mathvec.git`
- Install dependencies: `npm install`
- Run: 
```
       npm run-script build
       npm run-script dev
```
- To run test cases built within the repository: `npm test`

## Examples of how the library operates

### Utility
Utility/auxiliary functions that will be used in other codes such as: 
```
/** Create structure containing angle either in degrees and radians */
export function Angle(rad: number) {
  return { rad, deg: (rad / Math.PI) * 180 };
}
```
### Vector
[vector.ts](https://github.com/zolbooo/mathvec/blob/master/src/vector.ts) file calculates and returns different types of vector equations.
```
/** Structure representing N-dimensional vector */
export interface Vector extends Latexable {
  /** Length of vector. */
  length: number;
  /** Magnitude of vector. */
  magnitude: number;
  /** Coordinates of vector. */
  coordinates: readonly number[];

  /** Add two vectors. Returns new vector. */
  add(b: Vector): Vector;
  /** Subtract two vectors. Returns new vector. */
  sub(b: Vector): Vector;
  /** Multiply vector by scalar. Returns new vector. */
  mul(b: number): Vector;
  /** Find dot product of two vectors. */
  dot(b: Vector): number;
  /** Find angle between two vectors. */
  angle(b: Vector): ReturnType<typeof Angle>;

  /** Create new vector with opposite direction with same length. */
  neg(): Vector;
  /** Check if two vectors are equal. */
  equal(v2: Vector): boolean;
}
/** More below... */
```

### Point
[point.ts](https://github.com/zolbooo/mathvec/blob/master/src/point.ts) file includes interface representing point on the n dimensional plane which returns the calculated values in separate function.
```
export interface TPoint extends Latexable {
  /** Magnitude of point */
  magnitude: number;
  /** Coordinates of point */
  coordinates: readonly number[];

  /** Calculate vector between two points */
  to(p2: TPoint): Vector;
  /** Get middle of two points */
  mid(p2: TPoint): TPoint;
  /** Apply vector transformation on point */
  apply(vec: Vector): TPoint;
  /** Check if two points are equal. */
  equal(p2: TPoint): boolean;
}
/** More below... */
```

**Directional comments are written in the code which you can implement them to your app.
You can also add a little spice and use them for Figma, Adobe XD as a plugin.**
- Math Rocks! 🚀


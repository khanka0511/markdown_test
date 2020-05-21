# MathVec 🧮
Math library built with Typescript 

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

## Usage

##### Function Vec creates new Vector instance which has following methods:
```
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
```
For example:
```
  const a = Vec(1, -4, 3);
  const b = Vec(9, 4, 2);
  a.add(b); // Vec(10, 0, 5)
```

##### Function Point creates new TPoint instance. TPoint has following methods:
```
  /** Calculate vector between two points */
  to(p2: TPoint): Vector;
  /** Get middle of two points */
  mid(p2: TPoint): TPoint;
  /** Apply vector transformation on point */
  apply(vec: Vector): TPoint;
  /** Check if two points are equal. */
  equal(p2: TPoint): boolean; 
```
For example: 
```
  const a = Point(1, 1, 1);
  const b = Point(3, 3, 3);
  a.mid(b); //mid(2, 2, 2);
```

**Directional comments are written in the code which you can implement them to your app.
You can also add a little spice and use them for Figma, Adobe XD as a plugin.**
- Math Rocks! 🚀


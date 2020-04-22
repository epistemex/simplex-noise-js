SimplexNoise
===

A fast and optimized implementation of SimplexNoise (Perlin Noise based)
for JavaScript.

Simplex Noise / Perlin noise is extremely useful in both 2D and 3D
in creating procedural terrains, complex materials, turbulence modifiers,
visual effects, particles, (fractal) noise patterns and so forth.

Note: In this version only 3D noise has been implemented (use z=0 for 2D use).
I also use [0.0, 1.0] range for internal needs rather than the usual[-0.5, 0.5]
Can be used on client side as well as with Node.js.


Usage
-----

Create an instance of `SimplexNoise`:

```javascript
const sx = new SimplexNoise([seedArray]);
```

Then call `noise3D()` with normalized types of values for x, y and z.
Use `z=0` to get a value for 2D usage.

You can scale the values to get more details within a window:
```javascript
const noiseValue = sx.noise3D(x, y, z);
const noiseValue = sx.noise3D(x / width * scale, y / height * scale, 0);
```

Re-seed or use an existing seed-array:
```javascript
const seedArray = sx.getSeedArray();  // current seed-array
sx.seed();                            // new random seed-array
sx.seed(seedArray);                   // initialize with a former seed-array
```

License
---

MIT License.

(c) 2014-2016, 2018, 2024 epistemex

![Epistemex](https://i.imgur.com/GP6Q3v8.png)

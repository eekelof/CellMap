# CellMap

[![npm](https://img.shields.io/npm/v/@wingit/cellmap)](https://www.npmjs.com/package/@wingit/cellmap)
[![npm](https://img.shields.io/npm/dm/@wingit/cellmap)](https://www.npmjs.com/package/@wingit/cellmap)
[![GitHub](https://img.shields.io/github/license/eekelof/cellmap)](https://github.com/git/git-scm.com/blob/main/MIT-LICENSE.txt)

Spatial Hash Grid that extends Map

## Features

- :heavy_check_mark: Elements are stored on a 2D grid
- :heavy_check_mark: Filter nearby elements
- :heavy_check_mark: Extends Map
- :blue_square: Written in TypeScript

## Installation

#### Using npm
```bash
npm i @wingit/cellmap
```

#### Using bun
```bash
bun i @wingit/cellmap
```

## Usage
```javascript
import CellMap from "@wingit/cellmap";

// create a CellMap(width, height, cell size)
const units = new CellMap(100, 100, 10);

// add a unit
// set hash to -1, it is used internally and gets reassigned when added
const unit = { id: "1", hash: -1, pos: {x: 0, y: 0}, name: "Bob" };
units.set(unit.id, unit);

// delete a unit
units.delete("1");

// update a unit
unit.pos.x = 35;
units.update(unit);

// get cells in range
const cellsInRange = g.ig.units.query(pos, radius);
for (const cell of cellsInRange) {
    for (const u of cell){
        console.log(u);
    }
}
```

## License

MIT
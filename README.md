# Node Minecraft Data 26.2

Standalone Node.js package for the
[Complexity-ML Minecraft Java 26.2 dataset](https://github.com/Complexity-ML/minecraft-data-26.2).
It is the data layer used by GAME LAB's protocol and Mineflayer distributions.

| Package | Minecraft Java | Protocol | Data version |
| --- | --- | --- | --- |
| `minecraft-data@3.111.0+complexity.26.2.3` | 26.2 | 776 | 4903 |

## Install

The standalone package is distributed as an immutable GitHub Release asset:

```bash
npm install "https://github.com/Complexity-ML/node-minecraft-data-26.2/releases/download/complexity-26.2.3/minecraft-data-complexity-26.2.3.tgz"
```

Pin this exact URL in applications that must reproduce the GAME LAB 26.2
runtime. The archive includes all data files; consumers do not need to
initialize a Git submodule.

## Usage

```js
const minecraftData = require('minecraft-data')

const mcData = minecraftData('26.2')

console.log(mcData.version.minecraftVersion) // 26.2
console.log(mcData.version.version) // protocol 776
console.log(mcData.blocksByName.oak_log)
```

ES modules can import the same CommonJS entry point:

```js
import minecraftData from 'minecraft-data'

const mcData = minecraftData('26.2')
```

## Included data

The package exposes blocks, items, entities, biomes, recipes, sounds,
particles, effects, enchantments, protocol schemas and version metadata. It
also retains the historical datasets inherited from upstream.

## Validate from source

```bash
git clone --recurse-submodules https://github.com/Complexity-ML/node-minecraft-data-26.2.git
cd node-minecraft-data-26.2
npm install
npm test
```

The current release passes 888 package tests and 501,995 schema validations.

## Documentation

- [API reference](doc/api.md)
- [Data history](doc/history.md)
- [Raw 26.2 dataset](https://github.com/Complexity-ML/minecraft-data-26.2)
- [Releases](https://github.com/Complexity-ML/node-minecraft-data-26.2/releases)

## Maintenance

Open issues and pull requests in this repository for the Complexity-ML 26.2
package. Release archives are the supported installation surface.

## Credits and license

Derived from
[PrismarineJS node-minecraft-data](https://github.com/PrismarineJS/node-minecraft-data)
and [PrismarineJS minecraft-data](https://github.com/PrismarineJS/minecraft-data).
The upstream history and contributor attribution are retained. Complexity-ML
maintains this distribution independently and is not affiliated with Mojang or
Microsoft.

Licensed under MIT, as declared in [package.json](package.json).

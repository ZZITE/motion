# Luma

A global illumination library from [Framer](https://framer.com).

API subject to change before version `1.0`.

<p align="center">
  <a href="https://www.npmjs.com/package/luma" target="_blank">
    <img src="https://img.shields.io/npm/v/luma.svg?style=flat-square" />
  </a>
  <a href="https://www.npmjs.com/package/luma" target="_blank">
  <img src="https://img.shields.io/npm/dm/luma.svg?style=flat-square" />
  </a>
  <a href="https://twitter.com/framer" target="_blank">
  <img src="https://img.shields.io/twitter/follow/framer.svg?style=social&label=Follow"  />
  </a>
  <a href="https://discord.gg/DfkSpYe" target="_blank">
  <img src="https://img.shields.io/discord/308323056592486420.svg?logo=discord&logoColor=white" alt="Chat on Discord">
  </a>
</p>

## Usage

### React

Set up a global light.

```jsx
import { Light } from "luma"

export function App({ children }) {
    return (
        <Light x={-20} y={-40}>
            {children}
        </Light>
    )
}
```

Cast the light by generating a `boxShadow` property.

```jsx
import { useShadow } from "luma"

export function Component() {
    const depth = 10
    const boxShadow = useShadow(depth)

    return <div style={{ boxShadow }} />
}
```
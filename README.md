# frontity-with-tailwind
This is a example repo for using Frontity with Tailwindcss + babel-plugin-macros 

## Setup
`npm install --save tailwindcss babel-plugin-macros tailwind.macro@next`

## Config
`npx tailwindcss init --full` Here you include your new classes or modify one.

## Babel
Create the file: babel-pluginmacros.config.js with the followind content:

```
module.exports = {
  tailwind: {
    config: "./tailwind.config.js",
    format: "auto",
  },
};
```

## Use in your component
```
import React from "react";
import { connect, styled } from "frontity";
import Link from "./link";
import tw from "tailwind.macro";

const Button = styled("button")`
  ${tw`font-mono text-lg bg-blue-300`};
`;
```

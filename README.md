# Using Tailwindcss with Frontity
This is a example repo for using Frontity with Tailwindcss + babel-plugin-macros + babel-plugin-twin + twin.macro

## Setup
`yarn add -D tailwindcss babel-plugin-macros babel-plugin-twin twin.macro`

## Config (Optional)
`npx tailwindcss init --full` Here you include your new classes or modify one.

## Babel
Create the file: .babelrc with the following content:

```
{
  "plugins": ["babel-plugin-twin", "babel-plugin-macros"]
}
```

## Use in your component. Ex: src -> mars theme -> components -> index.js
```
import { Global, css, connect, styled, Head } from "frontity";
import Switch from "@frontity/components/switch";
import Header from "./header";
import List from "./list";
import Post from "./post";
import Loading from "./loading";
import Title from "./title";
import PageError from "./page-error";
import tw from "twin.macro";

const HeadContainer = styled.div`
  ${tw`flex flex-col items-center bg-gray-900 h-[200px]`};
`;
```

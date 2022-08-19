<p align="center" id="title">
  <img src="https://raw.githubusercontent.com/useverto/design/master/logo/logo_light.svg" alt="Verto logo (light version)" width="110" />

  <h3 align="center">Verto Flex</h3>

  <p align="center">
    An embeddable, programmable order book framework
  </p>
</p>

## Installation

```sh
npm install @verto/flex
```

or

```
yarn add @verto/flex
```

## Prerequisites

Install the [ArConnect](https://www.arconnect.io/) browser extension

Install ArLocal to test your smart contract locally
```
npx arlocal
```

Your SmartWeave contract state MUST contain the following variables in order for the Verto Components to function properly:

```js
{
  emergencyHaltWallet: "",
  halted: false,
  pairs: [],
  usedTransfers: [],
  invocations: [],
  foreignCalls: []
}
```
The state is stored in a JSON file

## Usage

This framework includes the core functions necessary to give SmartWeave contracts the ability to embed and manage a central limit order book.

### Import

To use the library, you'll need to import its functions

```ts
import {
  AddPair,
  CancelOrder,
  CreateOrder,
  Halt,
  ReadOutbox,
} from "@verto/flex";
```

### Add a pair

```ts
const { newState, result } = await AddPair(state, action);
```

### Cancel Order

```ts
const { newState, result } = await cancelOrder(state, action);
```

### Create Order

```ts
const { newState, result } = await cancelOrder(state, action);
```

### Halt

```ts
const { newState, result } = await halt(state, action);
```

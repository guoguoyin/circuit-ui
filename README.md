<div align="center">

[![Circuit UI Logo](./.github/logo.png)](https://circuit.sumup.com)

[Circuit UI](https://circuit.sumup.com) is the web incarnation of the [SumUp](https://sumup.com) Circuit Design System. Our primary goal is to create a system that can be used to build a wide variety of SumUp websites and apps, while providing a consistent user experience to our end users. In addition, the design system and component library should be easy to use for developers and designers.

</div>

## Table of Contents <!-- omit in toc -->

- [Getting started](#getting-started)
- [Installation](#installation)
- [Development](#development)
- [Deployment](#deployment)
- [Linting and formatting](#linting-and-formatting)
- [Testing](#testing)
- [Utils](#utils)
- [Creating components](#creating-components)
- [Contributing](#contributing)
- [About SumUp](#about-sumup)

## Getting started

Here are a few helpful links for getting started with Circuit UI:

- [Getting started](http://circuit.sumup.com/#/getting-started/developers) - Install and configure Circuit for your React app
- [Styles](http://circuit.sumup.com/#/styles/colors) - Learn about our foundations such as colors, spacing, and typography.
- [Guidelines](http://circuit.sumup.com/#/guidelines/content) - Use the design system in a compliant way.
- [Components](http://circuit.sumup.com/#/components/badge) - Explore the available UI components.

## Installation

```
yarn add @sumup/circuit-ui
```

## Development

```
yarn && yarn start
```

## Deployment

```
yarn deploy
```

## Linting and formatting

```
yarn unit:lint-js

yarn fix
```

## Testing

```
yarn test:unit:watch
```

```javascript
import React from 'react';
import Button from '.';

describe('Button', () => {
  it('should not render if there is no click handler, label, or children', () => {
    const button = create(<Button />);
    expect(button).toMatchSnapshot();
  });
  it('should take the body text as a child', () => {
    const output = mount(<Button onClick={() => {}}>Hello World</Button>);
    expect(output.text()).toContain('Hello World');
  });
});
```

## Utils

Besides the component library, we also export some utilities which you
might need in order to use the components. The three main ones:

- `numbersUtils` - a module for dealing with number localization.
- `currencyUtils` - a module for formatting currency amounts.
- `styleHelpers` - a module containing helpers for writing styles.

## Creating components

This project uses [@sumup/foundry](https://www.npmjs.com/package/@sumup/foundry) and the provided `plop` command to generate new React components. The functionality is exposed as the `create-component` npm script from package.json.

To create a new component, run `yarn create-component` inside the project. You'll see a CLI that guides you through the process.

After the CLI has finished, all files will have been created in the location you specified.

## Contributing

If you have ideas for how we could improve this readme or the project in general, [let us know](https://github.com/sumup/circuit-ui/issues) or [contribute some](https://github.com/sumup/circuit-ui/edit/master/README.md)!

## About SumUp

[SumUp](https://sumup.com) is a mobile-point of sale provider. It is our mission to make easy and fast card payments a reality across the _entire_ world. You can pay with SumUp in more than 30 countries, already. Our engineers work in Berlin, Cologne, Sofia, and Sāo Paulo. They write code in JavaScript, Swift, Ruby, Elixir, Erlang, and much more. Want to come work and with us? [Head to our careers page](https://sumup.com/careers) to find out more.

# React Native Animated Ellipsis
A simple, customizable animated dots component ideal for loading screens in React Native apps (forked from adorableio/react-native-animated-ellipsis - not maintained).

![Kinda like iOS](https://raw.githubusercontent.com/wiki/adorableio/react-native-animated-ellipsis/images/example_ios_ish.gif)


## Fixed Issues
1. `useNativeDriver` was not specified. This is a required option and must be explicitly set to `true` or `false`
2. `undefined` is not an object evaluating `_reactNative.Text.propTypes.style` - (Deprecated prop types)

## Installation

```sh
# yarn
yarn add @zfloc/react-native-animated-ellipsis

# npm
npm i @zfloc/react-native-animated-ellipsis
```

## Importing
```js
import AnimatedEllipsis from '@zfloc/react-native-animated-ellipsis';
```

## Usage
Just include the component in the output of any other component like this:

```jsx
render() {
  return (
    <View>
      <Text>
        Loading
        <AnimatedEllipsis />
      </Text>
    </View>
  );
}
```

which will get you something like this:

![Basic Example](https://raw.githubusercontent.com/wiki/adorableio/react-native-animated-ellipsis/images/example_basic.gif)


## Props
Customize the number of dots, animation speed, and style using these props:

| Property | Description |
|----------|-------------|
| **`numberOfDots`** | The number of dots you'd like to show. Defaults to **3**. |
| **`animationDelay`** | The length in milliseconds of each phase of the animated. Defaults to **300**. |
| **`minOpacity`** | The minimum opacity for the dots. Defaults to **0**. |
| **`style`** | CSS to apply to the dots. It accepts any styles that a normal `<Text />` component can take. |
| **`useNativeDriver`** | Specify true or false. Defaults to **true**. |


## More Examples

![Ten Dots Example](https://raw.githubusercontent.com/wiki/adorableio/react-native-animated-ellipsis/images/example_ten_dots.gif)

```jsx
<AnimatedEllipsis numberOfDots={10} />
```

------

![Complex Example](https://raw.githubusercontent.com/wiki/adorableio/react-native-animated-ellipsis/images/example_four_red_dots.gif)

```jsx
<AnimatedEllipsis 
  numberOfDots={4}
  animationDelay={150}
  style={{
    color: 'red',
    fontSize: 72,
  }}
/>
```

------

![Kinda like iOS](https://raw.githubusercontent.com/wiki/adorableio/react-native-animated-ellipsis/images/example_ios_ish.gif)

```jsx
<AnimatedEllipsis 
  numberOfDots={3}
  minOpacity={0.4}
  animationDelay={200}
  style={{
    color: '#94939b',
    fontSize: 100,
    letterSpacing: -15,
  }}
/>
```

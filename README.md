# Ken's navigation example
This was forked from vikeri's [re-navigate](https://github.com/vikeri/re-navigate). It brings you through a skeleton of react-components, using a simple (cond curren-state state1 [component1] state2 [component2]) structure. This cond inside one component may not be the right way to switch between scenes....seems to work, but may not be performant.

# re-navigate
> Example of React Native Navigation with [re-frame](https://github.com/Day8/re-frame)/[re-natal](https://github.com/drapanjanas/re-natal/)

This example uses React Native's new Navigation component [NavigationExperimental](https://github.com/ericvicenti/navigation-rfc) which has a more FRP-like setup (like redux) and thus it works ridiculously well with [re-frame](https://github.com/Day8/re-frame).

## Example code

It is based on the scaffold from [re-natal](https://github.com/drapanjanas/re-natal/), almost everything is found in [navigator-cljs.ios.core](src/navigator_cljs/ios/core.cljs)

## Run

Requirements: 
- node & npm
- leiningen `brew install leiningen`
- re-natal & react-native-cli `npm install -g re-natal react-native-cli` 

`cd` into the directory.

```
npm install && lein prod-build && react-native run-ios
```

## Notes

In the future this might become a library if it would be useful to reuse things like the [navigation handlers](src/navigator_cljs/handlers.cljs#L40-L62) and the [db schema](src/navigator_cljs/db.cljs#L5-L15).

It has only been tested with iOS but in theory it should work with Android as well since there are no iOS-specific components (I think).

## Structure for React Native project

Currently includes:

- React Native
- React Navigation
- Recoil
- TypeScript
- And more!

## Quick Start

The boilerplate project's structure will look similar to this:

```
project
├── app
│   ├── components
│   ├── i18n
│   ├── utils
│   ├── models
│   ├── navigators
│   ├── screens
│   ├── services
│   ├── theme
│   ├── app.tsx
├── storybook
│   ├── views
│   ├── index.ts
│   ├── storybook-registry.ts
│   ├── storybook.ts
│   ├── toggle-storybook.tsx
├── test
│   ├── __snapshots__
│   ├── storyshots.test.ts.snap
│   ├── mock-i18n.ts
│   ├── mock-reactotron.ts
│   ├── setup.ts
│   ├── storyshots.test.ts
├── README.md
├── android
│   ├── app
│   ├── build.gradle
│   ├── gradle
│   ├── gradle.properties
│   ├── gradlew
│   ├── gradlew.bat
│   ├── keystores
│   └── settings.gradle
├── ios
│   ├── Project
│   ├── Project-tvOS
│   ├── Project-tvOSTests
│   ├── Project.xcodeproj
│   └── ProjectTests
├── .env
├── ReactotronConfig.js
└── package.json

```

### ./app directory

It is the `app` directory. This is a directory you would normally have to create when using vanilla React Native.

The inside of the src directory looks similar to the following:

```
app
│── components
│   │── button
│       │── button.tsx
│       │── button.styles.ts
│       │── button.props.ts
│── i18n
├── models
├── navigators
├── screens
│   │── screen_name
│       │── screen_name.tsx
│       │── screen_name.styles.ts
│       │── screen_name.props.ts
├── services
├── theme
├── utils
└── app.tsx
```

**components**
This is where your React components will live. Each component will have a directory containing the `.tsx` file, along with a story file, and optionally `.presets`, `.atom`, and `.props` files for larger components. The app will come with some commonly used components like Button.

**i18n**
This is where your translations will live if you are using `react-native-i18n`.

**models**
This is where your app's models will live. Each model has a directory which will contain model file, test file, and any other supporting files like types, etc.

**navigators**
This is where your `react-navigation` navigators will live.

**screens**
This is where your screen components will live. A screen is a React component which will take up the entire screen and be part of the navigation hierarchy. Each screen will have a directory containing the `.tsx` file, along with any assets or other helper files.

**services**
Any services that interface with the outside world will live here (think REST APIs, Push Notifications, etc.).

**theme**
Here lives the theme for your application, including spacing, colors, and typography.

**utils**
This is a great place to put miscellaneous helpers and utilities. Things like date helpers, formatters, etc. are often found here. However, it should only be used for things that are truely shared across your application. If a helper or utility is only used by a specific component or model, consider co-locating your helper with that component or model.

**app.tsx** This is the entry point to your app. This is where you will find the main App component which renders the rest of the application.

### ./storybook directory

This is where your stories will be registered and where the Storybook configs will live.

### ./test directory

This directory will hold your Jest configs and mocks, as well as your [storyshots](https://github.com/storybooks/storybook/tree/master/addons/storyshots) test file. This is a file that contains the snapshots of all your component storybooks.

## Running Storybook

From the command line in your generated app's root directory, enter `yarn run storybook`
This starts up the storybook server and opens a story navigator in your browser. With your app
running, choose Toggle Storybook from the developer menu to switch to Storybook; you can then
use the story navigator in your browser to change stories.

## Additional links

- [Recoil.js](https://recoiljs.org/)
- [React+TypeScript Cheatsheets](https://github.com/typescript-cheatsheets/react)
- [DTO Pattern](https://www.baeldung.com/java-dto-pattern)
- [Model](https://www.tomdalling.com/blog/software-design/model-view-controller-explained/)
- [React Native + TypeScript](https://reactnative.dev/docs/typescript)
- [Reactotron](https://github.com/infinitered/reactotron)

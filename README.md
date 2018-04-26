# Expo & Yarn Workspaces

This is a simple set to show that expo doesn't work with yarn workspaces.

There are two packages dummy and expo.
* Dummy is just a single JS file that imports immutable
* Expo is a project create with 'exp init' and then had immutable added to it as well as set react-native and expo to be "nohoist" for yarn workspaces

yarn workspaces hoists the immutable module to the root node_modules

If you try to run the expo project in Expo XDE, you will get an error:

Unable to resolve module 'immutable' from '/HOME_DIR/expo-yarn-workspaces/packages/expo/App.js': Module 'immutable' does not exist in the Hast module map or in these directories: /HOMEDIR/expo-yarn-workspaces/node_modules

But immutable does exist in that directory.

## **Imports in the project files should have an order.**

# 1 - Global imports

First of all we need to import global libs like:

```js
 > import 'react-native-gesture-handler';
```

In this case we don't need to define a variable of the library, this type of import must be above the other imports. Normally it is not usual and it may occur rarely in each project.

# 2 - React/React-Native

After global imports we need to import React/React-native builtin Components/Functions and everything that we need of these librarys.

```js
import 'react-native-gesture-handler';

> Import React from 'react';
> import {View} from 'react-native';
```

# 3 - Installed Libraries

The third import step is about installed library. We need to import functions/components from installed library.

```js
import 'react-native-gesture-handler';

Import React from 'react';
import {View} from 'react-native';

> import {createStackNavigator} from '@react-navigation/stack';
> import {NavigationContainer} from '@react-navigation/native';
```

# 4 - Internal components

In each project we develop some components to scale and write less and develop more.
Forth step of import is internal components such as Common/Element and the other function/class base components.

```js
import 'react-native-gesture-handler';

Import React from 'react';
import {View} from 'react-native';

import {createStackNavigator} from '@react-navigation/stack';
import {NavigationContainer} from '@react-navigation/native';

> import {Header} from '@component/common';
```

# 5 - State-management(Store, Actions)

Another important part of our application is store and its functions (Actions).

```js
import 'react-native-gesture-handler';

Import React from 'react';
import {View} from 'react-native';

import {createStackNavigator} from '@react-navigation/stack';
import {NavigationContainer} from '@react-navigation/native';

import {Header} from '@component/common';

> import store from "@store/store";
> import {setPart} from "@store/part/actions";
```

# 6 - Helper/Utility functions

```js
import 'react-native-gesture-handler';

Import React from 'react';
import {View} from 'react-native';

import {createStackNavigator} from '@react-navigation/stack';
import {NavigationContainer} from '@react-navigation/native';

import {Header} from '@component/common';

import store from "@store/store";
import {setPart} from "@store/part/actions";

> import {getColorCode} from '@utility/helper/functionHelper';
> import navigationService from "@navigation/navigationService";
```

# 7 - Constants

```js
import 'react-native-gesture-handler';

Import React from 'react';
import {View} from 'react-native';

import {createStackNavigator} from '@react-navigation/stack';
import {NavigationContainer} from '@react-navigation/native';

import {Header} from '@component/common';

import store from "@store/store";
import {setPart} from "@store/part/actions";

import {getColorCode} from '@utility/helper/functionHelper';
import navigationService from "@navigation/navigationService";

> import {valueConstant} from '@utility/constants/valueConstant';
```

# 8 - Project assets (JSON, Image, Fonts)

```js
import 'react-native-gesture-handler';

Import React from 'react';
import {View} from 'react-native';

import {createStackNavigator} from '@react-navigation/stack';
import {NavigationContainer} from '@react-navigation/native';

import {Header} from '@component/common';

import store from "@store/store";
import {setPart} from "@store/part/actions";

import {getColorCode} from '@utility/helper/functionHelper';
import navigationService from "@navigation/navigationService";

import {valueConstant} from '@utility/constants/valueConstant';

> import defaultPartAvatar from '@assets/image/defaultPartAvatar.png'
```

# :tw-1f31f: Note:

1. You may need some of the above in different situations, so make sure you always prioritize.
2. Double-check when done your tasks and remove unused import(s).
3. Put a blank line between each section like the above example.

# Footnote:

This document is open to update and improve the conventions. So if you have any idea you can talk with team leader to double-check the conventions together.

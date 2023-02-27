### ReactNative 

``` javascript
import * as React from 'react';
import {View, StyleSheet,Text} from 'react-native';

export default function Footer() {
  return (
    <View style={styles.container}>
    <Text>이명헌</Text>
      <View style={styles.nav}>
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    backgroundColor: "pink",
  },
  nav: {
  },
});
```

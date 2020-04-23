# ReactNativeNote

# Android
For those who tried everything and still get this error:
import { Platform } from 'react-native';

const config = {
  server: Platform.select({
    ios: '127.0.0.1', // or 'localhost'
    android: '10.0.2.2',
  }),
};

config.apiEndpoint = `http://${config.server}:port/api`;
Explanation: iOS Simulators use the same environment as our programming environment (your computer), while Android emulators set up a new device with a different IP address, so their localhost doesn't match ours.

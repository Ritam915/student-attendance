# student-attendance
//sing up 
import {
  StyleSheet,
  Text,
  View,
  TextInput,
  StatusBar,
  ImageBackground,
  TouchableOpacity,
  Dimensions,
} from 'react-native';
import React from 'react';
import {useNavigation} from '@react-navigation/native';

const Signup = () => {
  const navigation = useNavigation();
  return (
    <View>
      <StatusBar backgroundColor={'#634cb4'} barStyle="light-content" />

      <ImageBackground
        source={{
          uri: 'https://w0.peakpx.com/wallpaper/611/54/HD-wallpaper-purple-paper-texture-paper-background-paper-texture-with-pattern-purple-creative-background.jpg',
        }}
        style={styles.View}>
        <View>
          <TextInput
            placeholder="USERNAME"
            style={{
              backgroundColor: '#fff',
              borderColor: 'black',
              width: '70%',
              borderRadius: 15,
              marginTop: 10,
              textAlign: 'center',
              marginHorizontal: '15%',
            }}></TextInput>
          <TextInput
            placeholder="PASSWORD"
            secureTextEntry
            style={{
              backgroundColor: '#fff',
              width: '70%',
              borderRadius: 15,
              textAlign: 'center',
              marginTop: 10,
              marginHorizontal: '15%',
            }}></TextInput>
        </View>
        <TouchableOpacity
          style={styles.log}
          onPress={() => navigation.navigate('mainscreen')}>
          <Text style={{fontSize: 30, textAlign: 'center'}}>Login</Text>
        </TouchableOpacity>
        <View
          style={{
            flexDirection: 'row',
            justifyContent: 'space-around',
            marginHorizontal: '10%',
            marginTop: 20,
          }}>
          <View>
            <TouchableOpacity>
              <Text
                style={{color: '#634cb4', fontSize: 20, fontWeight: 'bold'}}>
                Sign up
              </Text>
            </TouchableOpacity>
            <TouchableOpacity>
              <Text
                style={{color: '#634cb4', fontSize: 20, fontWeight: 'bold'}}>
                privacy policy
              </Text>
            </TouchableOpacity>
          </View>
          <View>
            <TouchableOpacity>
              <Text
                style={{color: '#634cb4', fontSize: 20, fontWeight: 'bold'}}>
                forgot password
              </Text>
            </TouchableOpacity>
            <TouchableOpacity>
              <Text style={{color: 'orange', fontSize: 20, fontWeight: 'bold'}}>
                User Manual
              </Text>
            </TouchableOpacity>
          </View>
        </View>
      </ImageBackground>
    </View>
  );
};

export default Signup;

const styles = StyleSheet.create({
  View: {
    height: '100%',
    width: '100%',
    justifyContent: 'center',
    // alignItems: 'center',
  },

  log: {
    height: 40,
    width: '70%',
    borderRadius: 10,
    backgroundColor: '#634cb4',
    marginTop: 10,
    marginHorizontal: '15%',
  },
});

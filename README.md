# React-Native
react native code
import React, {Component} from 'react';
import { View,
  StyleSheet,
  ImageBackground,
  Image,
  Text,
  TouchableOpacity

} from 'react-native';


export default class sendAppointment extends Component{
  constructor(props) {
    super(props)
    this.state = { count: 0 }
  }

  onPress = () => {
    this.setState({
      count: this.state.count+1
    })
  }
  
   render(){
     return(
      //MAIN VIEW
      <View style={StyleSheet.container}>
         <View>

              <ImageBackground
                style={{ width:'100%', height: 150, marginTop: 50 }}
                source={require('./resources/images/image3x.png')} >
                <Image
                  style={{ height: 140, width: 140, borderRadius: 140 / 2, marginTop:70, marginLeft:'32%'}}
                  source={require('./resources/images/kitten.png')} />
              </ImageBackground>

              <View>
                <Text style={{ color: '#4B4F64', fontSize: 14, marginLeft: 8,marginTop:60 }}> Phone Number </Text>
              </View>


              <View>
                <Text style={{ width: '40%', color: '#84868c', marginLeft: 13, fontSize: 12, marginTop:5  }}>
                  Enter Mobile Number
                </Text>
              </View>


              <View style={{ borderBottomColor: '#84868c', borderBottomWidth: 0.3,marginTop: -10, }} >
                <Text numberOfLines={1}>  </Text>
              </View>


              <View>
                <Text style={{ color: '#4B4F64', fontSize: 14, marginTop:6 , marginLeft: 8 }} > Status </Text>
              </View>


              <View>
                 <Text style={{ width: '100%', color: '#84868c', marginLeft: 13, fontSize: 12,marginTop:5, }}>
                  The Life Of Your Dream</Text>
              </View>


              <View style={{ borderBottomColor: '#84868c', borderBottomWidth: 0.3,margin:5 }} >
                <Text numberOfLines={1}>  </Text>
              </View>


              <View style={{ textAlign:'center',
              justifyContent:'space-between',
              flexDirection:'row' ,
              marginTop:25,
              }} >

               <TouchableOpacity style={{
                 justifyContent:'center',
                      marginLeft:25, 
                      width:120,
                      backgroundColor:'#0bc5b8',
                      height:35,
                      alignItems:'center',
                      borderRadius:15}} 
                      onPress={this.onPress}>
                    <Text style={{ color:'#ffffff', textAlign:'center',justifyContent:'center' , alignItems:'center' }}> 
                      Message 
                    </Text>
                </TouchableOpacity>
              

                   
                  <TouchableOpacity style={{
                    marginRight:25, 
                    width:120,
                    backgroundColor:'red',
                    height:35,
                    borderRadius:15,
                    justifyContent:'center',
                     }}
                    onPress={this.onPress}>
                    <Text style={{ color:'#ffffff',textAlign:'center',justifyContent:'center' , alignItems:'center'}}>
                      Block 
                    </Text>
                </TouchableOpacity>
               </View>


               <View style={{textAlign:'center',justifyContent:'center',marginTop:'40%',marginLeft:'25%'}} >
               <TouchableOpacity style={{
                 backgroundColor:'#16d097',
                 width:180,
                 height:35,
                 borderRadius:15,
                 justifyContent:'center',


               }} onPress={this.onPress}>
               <Text style={{ color:'#ffffff',textAlign:'center',justifyContent:'center' }}> Send Appointment </Text>
               </TouchableOpacity>
               </View>

          </View>
       </View>
     );
   }
 }

 const styles = StyleSheet.create({

  container:{
  flex:1,
  backgroundColor: 'white',
},



});


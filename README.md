# mech

//모터의 회전방향을 반환하는 함수이며 회전할 때만 실행되는 함수
int motorDirection(){
 if (sensor_xor()==0){
 boolean sensor1_init=sensor1_read();
 boolean sensor2_init=sensor2_read();
 int flag=0;
 while(flag==0){
 sensor1=sensor1_read();
 sensor2=sensor2_read();
 if (sensor1!=sensor1_init){
 clockwise=1;
 flag=1;
 }
 
 elseif (sensor2!=sensor2_init){
 clockwise=2;
 flag=1;
 }
 
 }
 }
 else{
 boolean sensor1_init=sensor1_read();
 boolean sensor2_init=sensor2_read();
 int flag=0;
 while(flag==0){
 sensor1=sensor1_read();
 sensor2=sensor2_read();
 if (sensor1!=sensor1_init){
 clockwise=2;
 flag=1;
 }
  elseif (sensor2!=sensor2_init){
    clockwise=1;
    flag=1;
  }
 
   }
 }
 return clockwise;
}


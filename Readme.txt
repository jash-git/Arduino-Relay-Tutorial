Arduino 繼電器 教學範例(Arduino Relay Tutorial)

資料來源: https://crazymaker.com.tw/arduino-how-to-use-relay/

01.繼電器介紹
02.繼電器規格
03.電路連接
04.Arduino程式

char Num; 
void setup() {
 pinMode(8,OUTPUT);
 Serial.begin(9600);
}

void loop() {
  //讀取序列埠傳入的字元
  if(Serial.available()){
    Num=Serial.read();
    Serial.println(Num);
  } 
  delay(10);
  if(Num=='1'){
    digitalWrite(8,LOW); //低電平觸發，LOW時繼電器觸發
  }
  else{
    digitalWrite(8,HIGH);
  }
}
# monu
piyush
int monu[3][3] = {{1,0,1},
                  {1,0,1},
                  {1,1,1}};
int rowpin[] = {2,5,7,};
int columnpin[] = {3,4,6,};             

void setup() {
 Serial.begin(9600);
 for(int i=0;i<3;i++)
 {
  pinMode(rowpin[i],OUTPUT );
 }
 for(int i=0; i<3;i++)
 {
  pinMode(columnpin[i],OUTPUT);
 }
}

void loop() {
  // put your main code here, to run repeatedly:
for(int i=0;i<3 ;i++ )
{
  digitalWrite(rowpin[i],LOW);
  for(int j=0; j<3 ; j++ )
  {
    if(monu[i][j] == 1)
    {
       digitalWrite(columnpin[j],HIGH);
    }
    else
    {
      digitalWrite(columnpin[j],LOW);
    }
    
  }
  delay(10);
}
Serial.println("///////////");
delay(1000);
}

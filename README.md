# ultrasonic
link to tinkercad "https://www.tinkercad.com/things/0yJauF69V69-ultrasonic-/editel"
```
const int trigPin = 9;
const int echoPin = 10;
// defines variables
long duration;
int distance;
void setup() {
  pinMode(8,OUTPUT);
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
  pinMode(echoPin, INPUT); // Sets the echoPin as an Input
  Serial.begin(9600); // Starts the serial communication
}
void loop() {
  // Clears the trigPin
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  // Sets the trigPin on HIGH state for 10 micro seconds
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  // Reads the echoPin, returns the sound wave travel time in microseconds
  duration = pulseIn(echoPin, HIGH);
  // Calculating the distance
  distance = duration * 0.034 / 2;
  // Prints the distance on the Serial Monitor
  Serial.print("Distance: ");
  Serial.println(distance);
  if (distance<=50){
    digitalWrite(8,1);
  }
  else 
    digitalWrite(8,0);
}
```
![Screenshot 2023-08-05 105131](https://github.com/Memo0302/ultrasonic/assets/92684739/cf1e4cef-bbd5-493b-9a0a-8a79e6ac288f)




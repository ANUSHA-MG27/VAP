#include <Servo.h>

// Define objects and constants
Servo servo;
const int trigPin = 11;
const int echoPin = 12;
const int distanceThreshold = 100; // Distance threshold in cm
long duration;
int distance;
const int delayTime = 2000; // Time delay in milliseconds (2 seconds)

void setup() {
  servo.attach(13);            // Attach servo to pin 13
  pinMode(trigPin, OUTPUT);    // Set trigPin as OUTPUT
  pinMode(echoPin, INPUT);     // Set echoPin as INPUT
}

void loop() {
  // Measure distance
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  
  duration = pulseIn(echoPin, HIGH);

  // Check for invalid duration and calculate distance
  if (duration > 0) {
    distance = duration * 0.034 / 2; // Convert duration to distance in cm
  } else {
    distance = 100; // Set to a default maximum distance if pulseIn times out
  }

  // Control servo based on distance with time delay
  if (distance >= distanceThreshold) {
    servo.write(90); // Move servo to 180°
    delay(delayTime); // Wait for specified delay time
  } else {
    servo.write(180); // Move servo to 90°
    delay(delayTime); // Wait for specified delay time
  }
}



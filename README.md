# Opening-Door
#include <Servo.h>

// Create a Servo object
Servo myServo;

// Define the pin for the servo
const int servoPin = 9;

// Define angles for open and closed positions
const int openAngle = 90;  // Angle to open the door
const int closedAngle = 0; // Angle to close the door

void setup() {
  // Attach the servo to the pin
  myServo.attach(servoPin);

  // Initialize the door to the closed position
  myServo.write(closedAngle);
}

void loop() {
  // Open the door
  openDoor();
  delay(5000); // Keep the door open for 5 seconds

  // Close the door
  closeDoor();
  delay(5000); // Keep the door closed for 5 seconds
}

void openDoor() {
  myServo.write(openAngle);
  delay(1000); // Wait for the servo to reach the position
}

void closeDoor() {
  myServo.write(closedAngle);
  delay(1000); // Wait for the servo to reach the position
}

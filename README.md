# -smart-energy-monitoring-arduino-
// Smart Energy Monitoring System ⚡
// Example Arduino sketch for reading current sensor

int sensorPin = A0; 
float voltage, current;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(sensorPin);
  voltage = sensorValue * (5.0 / 1023.0);
  current = voltage * 10; // Example conversion factor
  Serial.print("Current: ");
  Serial.print(current);
  Serial.println(" A");
  delay(1000);
}

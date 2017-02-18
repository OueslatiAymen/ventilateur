# ventilateur
arduino project aims to contorol a ventilator according to sensor's values 




# define valCaptmV 8
#define capteurLM35 A0
void setup() {
  Serial.begin(9600);
  pinMode(ventiloout, OUTPUT);

}

void loop() {
  float valCaptTemp = analogRead(capteurLM35);
  Serial.print("ADC: ", valCaptTemp);
  float vaCaptmV = ((valCaptTemp * 5000) / 1023);
  Serial.print("   mV: ", valCaptmV);
  float valCaptCelsus = vaCaptmV / 10
  if (tempC > 39) {
    digitalWrite(valCaptmV, HIGH);
    Serial.println('1');
    delay(250);

  }

  else {
    digitalWrite(valCaptmV, LOW);
    Serial.println('0');
    delay(250);


  }

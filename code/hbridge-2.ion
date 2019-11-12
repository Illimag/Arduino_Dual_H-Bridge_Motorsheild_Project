// Motor A
int IN1 = 7;
int IN2 = 8;

// Motor B
int IN3 = 10;
int IN4 = 11;

void stop() {
  // Motor A
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, LOW);

  // Motor B
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, LOW);
}

void forward() {
  // Motor A
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);

  // Motor B
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);  
}

void backward() {
  // Motor A
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, HIGH);

  // Motor B
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, HIGH);  
}

void setup() {
  Serial.begin(19200);
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);
  pinMode(IN3, OUTPUT);
  pinMode(IN4, OUTPUT);
  stop();
  Serial.println("Startup");
}

void loop() {
  char c = Serial.read();

  if (c == 'f') {
    Serial.println("Moving forward for 2 seconds");
    forward();
    delay(2000);
    stop();
  }
  
  if (c == 'b') {
    Serial.println("Moving backward for 2 seconds");
    backward();
    delay(2000);
    stop();
  }
  
}

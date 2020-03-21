# BlinkName
my code on blinking led on particle
// I have used the example code available on particle.io to blink an LED and modified the code to blink my first name in morse code

//initialising led on the particle
int led1 = D0; 
int led2 = D7; 

void setup() {

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);

}


void dot() {
    
    // the code in this function will allow the led light to stay on for a specific duration of time to represent a dot in the morse code
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    
    delay(200);
    
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);

 
    delay(200);
    
}

void dash() {
    
    // the code in this function will allow the led light to stay on for a specific duration of time to represent a dash in the morse code. this will be longer than the duration of a dot.
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    
    delay(600);
    
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);

 
    delay(200);
    
}

void space() {
    
    
    // the code in this function will allow the led light to stay off for a specific duration of time to signal a space in between each letter.
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);

 
    delay(500);
}
void loop() {
    
  // first letter of name: D (in morse code= -..)
  dash();
  dot();
  dot();
  space();
  //second letter of name: I (in morse code= ..)
  dot();
  dot();
  space();
  //third letter of name: N (in morse code= -.)
  dash();
  dot();
  space();
  //fourth letter of name: A (in morse code= .-)
  dot();
  dash();
  space();
  
}


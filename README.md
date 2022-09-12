# Blink_name

String name_user = ""; 
char user[50]; 
char my_first_name[] = "kanika";
char my_last_name[] = "kukreja";

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600); 

}

void dot()
{
  digitalWrite(LED_BUILTIN, HIGH);
  delay(600);
  digitalWrite(LED_BUILTIN, LOW);
  delay(600);
}

void dash()
{
  digitalWrite(LED_BUILTIN, HIGH);
  delay(3000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000); 
}

void loop() {

  if(Serial.available() == 0)
  {
    Serial.println("Enter your name: ");
    name_user = Serial.readString(); 
    name_user.toCharArray(user, name_user.length());
    for(int i = 0; i< strlen(user); i++)
    {
      char n = user[i]; 
      morse_encryption(n);
    }
  }

  else
  {
    for(int i = 0; i< strlen(my_first_name); i++)
    {
      char m = my_first_name[i]; 
      morse_encryption(m);
    }
    
  }

}


//This function will be able to convert each character 
//into it's morse code. 
void morse_encryption(char name)
{
   switch (name)
   {
    case 'a':
      dot();
      dash();
    break; 

    case 'b':
      dash();
      dot();
      dot();
      dot();
    break; 

    case 'c':
      dash();
      dot();
      dash();
      dot();
    break; 

    case 'd':
      dash();
      dot();
      dot();
    break; 

    case 'e':
      dot();
    break; 

    case 'f':
      dot();
      dot();
      dash();
      dot();
    break; 

    case 'g':
      dash();
      dash();
      dot();
    break; 

    case 'h':
      dot();
      dot();
      dot();
      dot();
    break; 

    case 'i':
      dot();
      dot();
    break; 

    case 'j':
      dot();
      dash();
      dash();
      dash();
    break; 

    case 'k':
      dash();
      dot();
      dash();
    break; 

    case 'l':
      dot();
      dash();
      dot();
      dot();
    break; 

    case 'm':
      dash();
      dash();
    break; 

    case 'n':
      dash();
      dot();
    break; 

    case 'o':
      dash();
      dash();
      dash();
    break; 

    case 'p':
      dot();
      dash();
      dash();
      dot();
    break; 

    case 'q':
      dash();
      dash();
      dot();
      dash();
    break; 

    case 'r':
      dot();
      dash();
      dot();
    break; 

    case 's':
      dot();
      dot();
      dot();
    break; 

    case 't':
      dash();
    break; 

    case 'u':
      dot();
      dot();
      dash();
    break; 

    case 'v':
      dot();
      dot();
      dot();
      dash();
    break; 

    case 'w':
      dot();
      dash();
      dash();
    break; 

    case 'x':
      dash();
      dot();
      dot();
      dash();
    break; 

    case 'y':
      dash();
      dot();
      dash();
      dash();
    break; 

    case 'z':
      dash();
      dash();
      dot();
      dot();
    break; 

    default: 
    digitalWrite(LED_BUILTIN,LOW);

    }
   
   }

# 1110

```c++
int x=0;
void setup() {
  pinMode(3, OUTPUT);
  pinMode(2, INPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  digitalWrite(3, HIGH);    
  digitalWrite(4, HIGH);
  digitalWrite(5, HIGH);
  digitalWrite(6, HIGH);
}

void loop() {

  if (digitalRead(2)==0)
  {
    delay(200);
    x= x+1;
  }
  switch (x)
  {
    case 0 :
    for (int i=3;i<6;i++)
    {
      digitalWrite(i, HIGH);
    }
    break;
    case 1 :
    digitalWrite(3, LOW);
    digitalWrite(6, HIGH);
    break;
    case 2 :
    digitalWrite(4, LOW);
    digitalWrite(3, HIGH);
    break;
    case 3 :
   digitalWrite(5, LOW);
   digitalWrite(4, HIGH);
    break; 
    case 4 :
    digitalWrite(6, LOW);
    digitalWrite(5, HIGH);
    break; 
  }
  if(x>4)
  x=1;

  }
```

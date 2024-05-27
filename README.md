const int SEMAFORO_A_VERDE = 8;
const int SEMAFORO_A_AMARILLO = 9;
const int SEMAFORO_A_ROJO = 10;

const int SEMAFORO_B_VERDE = 11;
const int SEMAFORO_B_AMARILLO = 12;
const int SEMAFORO_B_ROJO = 13;

const int SEMAFORO_C_VERDE = 2;
const int SEMAFORO_C_AMARILLO = 3;
const int SEMAFORO_C_ROJO = 4;

void setup() {
  pinMode(SEMAFORO_A_VERDE, OUTPUT);
  pinMode(SEMAFORO_A_AMARILLO, OUTPUT);
  pinMode(SEMAFORO_A_ROJO, OUTPUT);

  pinMode(SEMAFORO_B_VERDE, OUTPUT);
  pinMode(SEMAFORO_B_AMARILLO, OUTPUT);
  pinMode(SEMAFORO_B_ROJO, OUTPUT);

  pinMode(SEMAFORO_C_VERDE, OUTPUT);
  pinMode(SEMAFORO_C_AMARILLO, OUTPUT);
  pinMode(SEMAFORO_C_ROJO, OUTPUT);
}

void loop() {
  // Semáforo A en verde, semáforos B y C en rojo
  digitalWrite(SEMAFORO_A_VERDE, HIGH);
  digitalWrite(SEMAFORO_A_AMARILLO, LOW);
  digitalWrite(SEMAFORO_A_ROJO, LOW);
  
  digitalWrite(SEMAFORO_B_VERDE, LOW);
  digitalWrite(SEMAFORO_B_AMARILLO, LOW);
  digitalWrite(SEMAFORO_B_ROJO, HIGH);

  digitalWrite(SEMAFORO_C_VERDE, LOW);
  digitalWrite(SEMAFORO_C_AMARILLO, LOW);
  digitalWrite(SEMAFORO_C_ROJO, HIGH);

  delay(10000); // Espera 10 segundos en verde para semáforo A

  // Amarillo para Semáforo A, Semáforo B igual a rojo
  digitalWrite(SEMAFORO_A_VERDE, LOW);
  digitalWrite(SEMAFORO_A_AMARILLO, HIGH);
  
  digitalWrite(SEMAFORO_B_ROJO, HIGH);
  digitalWrite(SEMAFORO_B_AMARILLO, HIGH);
  digitalWrite(SEMAFORO_B_VERDE, LOW);

  delay(2000); // Espera 2 segundos en amarillo para semáforo A y B
  
  // Apagar LEDs de rojo y amarillo para Semáforo B
  digitalWrite(SEMAFORO_B_ROJO, LOW);
  digitalWrite(SEMAFORO_B_AMARILLO, LOW);

  // Rojo para Semáforo A, Verde para B
  digitalWrite(SEMAFORO_A_AMARILLO, LOW);
  digitalWrite(SEMAFORO_A_ROJO, HIGH);
  
  digitalWrite(SEMAFORO_B_VERDE, HIGH);

  delay(10000); // Espera 10 segundos en verde para semáforo B

  // Amarillo para Semáforo B, Semáforo C igual a rojo
  digitalWrite(SEMAFORO_B_VERDE, LOW);
  digitalWrite(SEMAFORO_B_AMARILLO, HIGH);
  
  digitalWrite(SEMAFORO_C_ROJO, HIGH);
  digitalWrite(SEMAFORO_C_AMARILLO, HIGH);
  digitalWrite(SEMAFORO_C_VERDE, LOW);

  delay(2000); // Espera 2 segundos en amarillo para semáforo B y C
  
  // Apagar LEDs de rojo y amarillo para Semáforo C
  digitalWrite(SEMAFORO_C_ROJO, LOW);
  digitalWrite(SEMAFORO_C_AMARILLO, LOW);

  // Rojo para Semáforo B, Verde para C
  digitalWrite(SEMAFORO_B_AMARILLO, LOW);
  digitalWrite(SEMAFORO_B_ROJO, HIGH);
  
  digitalWrite(SEMAFORO_C_VERDE, HIGH);

  delay(10000); // Espera 10 segundos en verde para semáforo C

  // Amarillo para Semáforo C, Semáforo A igual a rojo
  digitalWrite(SEMAFORO_C_VERDE, LOW);
  digitalWrite(SEMAFORO_C_AMARILLO, HIGH);
  
  digitalWrite(SEMAFORO_A_ROJO, HIGH);
  digitalWrite(SEMAFORO_A_AMARILLO, HIGH);
  digitalWrite(SEMAFORO_A_VERDE, LOW);

  delay(2000); // Espera 2 segundos en amarillo para semáforo C y A

  // Apagar LEDs de rojo y amarillo para Semáforo A
  digitalWrite(SEMAFORO_A_ROJO, LOW);
  digitalWrite(SEMAFORO_A_AMARILLO, LOW);

}

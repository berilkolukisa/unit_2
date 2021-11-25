// C++ code
//
int portA=2;
int portB=3;
int portC=4;
int portD=5;
int portE=6;
int portF=7;
int portG=8;



void setup()
{
  pinMode(portA,OUTPUT);
  pinMode(portB,OUTPUT);
  pinMode(portC,OUTPUT);
  pinMode(portD,OUTPUT);
  pinMode(portE,OUTPUT);
  pinMode(portF,OUTPUT);
  pinMode(portG,OUTPUT);
  
}

void loop ()
{
 bool X=false;
 bool Y=true;
 bool Z=true;
 bool W=true;
  
 //
 
 int A = ( !X && W ) || (Y && Z) || (Y && !W && !Z) || (X && !W &&Z) || (W && !Z && !Y) && (!X && !Y && !Z); 
 digitalWrite(portA, A);
  
 int B= (!Y && !Z) || (!Z && Y && !X) || (Z && !Y && !X) ||(!W && Y && X) || (W && !Y &&X);
 digitalWrite(portB, B);
  
 int C=(!Y && !X && !W) || (X && !Y && !W)|| (W && X && !Y) || (W && !Z && !X) || (Y && W && !Z) || (Y && Z && !W) || (Y && Z && !W); 
 digitalWrite(portC,C);
  
 int D=(!W && !Z && !X ) || (!Y && !X && W) || (Y && !X && Z) || (!Y && X && !Z);
 digitalWrite(portD,D); 
  
 int E= (!W && !Z && !X) || (!W && Y && !X) ||(W && !Z && !X) || ( W && Y) || (W && Z && X);
 digitalWrite(portE,E);
  
 int F= (Y && W )|| (Z && !W && !X) || (!X && !Y && !Z) || (W && !Z && !Y) || (Z && !W && !Y);
 digitalWrite(portF,F);

 int G=(W && Y) || (W && !Z && !X) || (!W && Z && !X) || (W && !Z && X) || (Z && !Y && X) ||(!W && !Z  && Y);
 digitalWrite(portG,G);
 
}

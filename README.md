# 2024-Steve
Idabel Kiamichi Tech robot program for Botball.
#include <kipr/wombat.h>

int main()
    //0 is left wheel
    //1 is right wheel
    //3 is arm
    //2 is claw
    //1950 down
    //505 open
{
    enable_servos();   
    
    set_servo_position(3,1000); //Port 3 servo is where our arm starts at
    set_servo_position(2,730); //Port 2 servo is how open our claw is
    msleep(2000); 
    
    set_servo_position(3,1950); //Bringing claw down while both motors are moving toward out first goal
    motor(0,80);
    motor(1,100);
    msleep(4550);
    
    set_servo_position(2,950); //closing the claw on the Moonbase door
    msleep(500);
    
    motor(0,-100); //while our claw is closed we move backward and pull the door open
    motor(1,-100);
    msleep(1000);
    
    set_servo_position(2,730); //releasng the claw from door
    msleep(1000);
    
    set_servo_position(3,1000); //bringing up the claw and turning our robot to where our Astronauts are 
    motor(0,100);
    motor(1,-50);
    msleep(1500);
    
    set_servo_position(2,430); //Reopens the claw while moving back to set us up for picking our goal up
    motor(0,-100);
    motor(1,-90);
    msleep(1000);
    
    motor(0,25);
    msleep(300);
    
    set_servo_position(3,2000); //brings our arm down around our astronauts
    ao();
    msleep(1000);
    
    set_servo_position(2,1500); //grips our claw around our astronauts
    msleep(1000);
  
    
    return 0;
    
}

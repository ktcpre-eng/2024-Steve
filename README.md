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
    
    set_servo_position(3,1000);
    set_servo_position(2,730);
    msleep(2000);
    
    set_servo_position(3,1950);
    motor(0,80);
    motor(1,100);
    msleep(4550);
    
    set_servo_position(2,950);
    msleep(500);
    
    motor(0,-100);
    motor(1,-100);
    msleep(1000);
    
    set_servo_position(2,730);
    msleep(1000);
    
    set_servo_position(3,1000);
    motor(0,100);
    motor(1,-50);
    msleep(1500);
    
    set_servo_position(2,430);
    motor(0,-100);
    motor(1,-90);
    msleep(1000);
    
    motor(0,25);
    msleep(300);
    
    set_servo_position(3,2000);
    ao();
    msleep(1000);
    
    set_servo_position(2,1500);
    msleep(1000);
  
    
    return 0;
    
}

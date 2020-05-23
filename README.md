# basic-meccanum-wheel-code
/*hello everybody, and welcome to our team github! if you want to watch a video tutorial on the following code, go to: https://www.youtube.com/watch?v=Y0AwXy4jGZY&amp;t=71s*/

import com.qualcomm.robotcore.hardware.HardwareMap;
import com.qualcomm.robotcore.hardware.DcMotorSimple;
import com.qualcomm.robotcore.hardware.DcMotor;
import com.qualcomm.robotcore.eventloop.opmode.Disabled;
import com.qualcomm.robotcore.eventloop.opmode.Autonomous;
import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;



@Autonomous
//extend class to LinearOpMode
public class GyroTester extends LinearOpMode {
 
  private DcMotor rightmotor;
  private DcMotor backrightmotor;
  private DcMotor leftmotor;
  private DcMotor backleftmotor;
 
	
	
	
	
		// todo: write your code here
	
	@Override
	public void runOpMode() throws InterruptedException{
 	
 	
 	rightmotor = hardwareMap.dcMotor.get("rightmotor");
	backrightmotor = hardwareMap.dcMotor.get("backrightmotor");
	leftmotor = hardwareMap.dcMotor.get("leftmotor");
	backleftmotor = hardwareMap.dcMotor.get("backleftmotor");
 	
 	
  	waitForStart();
  	
 	while (opModeIsActive() && !isStopRequested()){
     	
            rightmotor.setPower(0.5);
leftmotor.setPower(0.5);
backleftmotor.setPower(0.5);
backrightmotor.setPower(0.5);

sleep(500);

rightmotor.setPower-(0.5);
leftmotor.setPower(0.5);
backleftmotor.setPower(0.5);
backrightmotor.setPower(-0.5);

sleep(1000);

rightmotor.setPower(0.5);
leftmotor.setPower(-0.5);
backleftmotor.setPower(-0.5);
backrightmotor.setPower(0.5);

sleep(800);
  	
     	
     	
     	
 	}
	}
	
}

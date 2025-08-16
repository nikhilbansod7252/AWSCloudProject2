# AWSCloudProject2 ⛳
EC2 Instance Automation| Using AWS Services – EC2, Lambda, Event Bridge, IAM  

Problem Statment - We have 10 EC2 instance have to stop all at night 12pm and start at 7am  


Step1 - launch 10 EC2 instance  

Step2 - for automation use lambda where we create lambda funcations 1 for stop and 1 for start - this is root service wich stop and start ec2 instances  

Step3 - as lambda function dont have permissions to communicate with ec2 so we attach role to it having only permissions to start and stop ece  

Step4 - created ploicy only to start and stop ec2 and attached to IAM Role which is attached to lambda  

        -----------------------------------------------------------
        Trusted entity - Lambda - to whom u are attaching IAM Role
        Ploicy - EC2
        -----------------------------------------------------------
Step5 - Lambda function is in rest state so someone needs to trigger based on scheduled time ie: EventBridge  

Step6 - Create rule1 to trigger lambda stop at scheduled time and  rule2 to trigger lambda start at scheduled time using Cron Expression  

Step7 - you will see logs in Clous Watch Service 
<img width="680" height="167" alt="Capture" src="https://github.com/user-attachments/assets/5b881803-e8ee-4336-9144-fdd714e72fbf" />


EC2 Instance Automation| Using AWS Services – EC2, Lambda, Event Bridge, IAM | GitHub  

	Implemented a fully automated solution to start and stop Amazon EC2 instances based on a predefined schedule to optimize cost and resource  

   and resource utilization.  
   
	Developed two separate AWS lambda funcations – one is start and another stop EC2 instances capable of handling multiple instances  

   Simultaneously.  
   
	Create custom IAM role to lambda function, granting only necessary permissions to enable secure communication with EC2.  

	Utilizes Amazon Event Bridge to configure cron-expression rules that automatically trigger lambda function at specific time, ensuring consistent   

   uptime during business hours and reducing costs after hours.

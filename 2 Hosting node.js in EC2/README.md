HOST NODE JS APPLICATION IN AWS EC2

1. Launch an EC2 Instance
1.	Go to AWS EC2 Console: https://console.aws.amazon.com/ec2
2.	Click Launch Instance
3.	Choose:
o	Amazon Linux 2 AMI (or Ubuntu)
o	t2.micro (Free Tier)
o	Configure storage and firewall: allow port 22 (SSH) and port 3000 (or your app’s port)
4.	Download the .pem key pair (important for SSH)

2 Connect to Your EC2 Instance
Download your-key.pem file in ssh
ssh -i your-key.pem ec2-user@<EC2_PUBLIC_IP>
Replace your-key.pem and EC2_PUBLIC_IP with your actual values.

3 Install Node.js and Git (if not already installed)
For Amazon Linux 2:
sudo yum install -y nodejs git


4 Clone from GitHub if it's hosted there:
git clone <your-repo-url>
cd your-repo-folder

5 Install Dependencies
npm install





6 Start the Node.js Application
npm start



7 Steps to Allow Port 3000:
1.	Go to AWS EC2 Console
2.	Select your EC2 instance
3.	Under Security > Security Groups, click on the group name
4.	Go to the Inbound Rules tab
5.	Click Edit inbound rules
6.	Add a rule:
o	Type: Custom TCP
o	Port Range: 3000
o	Source: 0.0.0.0/0 (or restrict to your IP for security)


8 Access the App in Browser

http://<your-ec2-public-ip>:3000
Replace <your-ec2-public-ip> with your actual IP, for example:



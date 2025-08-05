**Deploying SQL Server Databases on Amazon RDS**

**Create an RDS SQL Server Instance**
1.	Navigate to RDS Dashboard > Databases > Create database
2.	Choose Standard create
3.	Engine options:Select Microsoft SQL Server
o	Choose edition: Express, Web, Standard, or Enterprise
4.	Set DB instance identifier, master username, and password
5.	Choose instance type (e.g., db.t3.medium)
6.	Set Storage size and type (e.g., General Purpose SSD)

**Connecting to the SQL Server Instance**

**Using SQL Server Management Studio (SSMS):**
1.	Open SSMS
2.	Server name: <endpoint-from-AWS-RDS> (e.g., mydb.xxxxx.us-east-1.rds.amazonaws.com)
3.	Authentication: SQL Server Authentication
4.	Enter username and password you set earlier



**Deploy Your Database
Once connected:**
•	You can create databases, run SQL scripts, import .bak files, or restore from S3 (if enabled via option group).


•	Do not expose RDS to the public internet in production
•	Use IAM roles and KMS encryption
•	Regularly automate snapshots
•	Monitor via Amazon CloudWatch
•	Configure alarms for CPU, memory, storage, etc.
•	Enable Enhanced Monitoring



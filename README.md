# IAM
### (identity and Access Managment)
Its a global service (doesnt matter in which region i create the user, available everywhere)

Composed of:
- Root account created by default (follow best practices)
- Users
  - can be in groups (can't contain other groups, not all users need a group, a user can be in multiple groups)
  - can be in Organizations

IAM Policy = permissions a user can be assigned a JSON document where we tell what they are allowed to do. least privilege best practice.
Consists of:
- "version": the policy version
- "Id": id for the policy (optional)
- "Statement": required
  - "Sid": identifier (optional)
  - "Effect": allow/deny access to certain APIs
  - "Principal": account/user/role its applied to
  - "Action": API calls that will be allowed / denied based on the effect
  - "Resource": list of res. to which the action is applied
  - "Contition": when its applied (optional)

Defense mechanisms:
- password policy (length/special chars/numbers/pass expiration, prevent reuse)
- MFA

To access AWS:
- AWS managment console (pw + MFA)
- CLI (access keys)
- SDK (access keys)
Access keys are generated with the AWS console, users manage their keys and are secret like passwords.

IAM Roles:
some AWS services will need to perform actions on your behalf, ex: you give permissions to your EC2 instance to do stuff on your AWS.
to do so you need to assign a ROLE to EC2

IAM security tools:
- IAM Credentials report (list of account user status and credentials)
- IAM Accesso advisor (shows the permissions granted to a user and when were last accessed)

IAM Best practices: 
- dont use the root account exept setup
- one phisical user per AWS user
- Assign user to grous and give permissions to groups not each user
- stong password policy
- MFA
- create and use Roles for givin perms. to AWS services
- Use access keys for CLI and SDK
- audit permissions w/ Credential report and IAM access advisor










# EC2

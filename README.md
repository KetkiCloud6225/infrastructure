# Assignment 3

## AWS Networking Setup
    
Here is what you need to do for networking infrastructure setup:

1. Create Virtual Private Cloud (VPC) (Links to an external site.).
2. Create subnets (Links to an external site.) in your VPC. You must create 3 subnets, each in a different availability zone in the same region in the same VPC.
3. Create an Internet Gateway (Links to an external site.) resource and attach the Internet Gateway to the VPC.
4. Create a public route table (Links to an external site.). Attach all subnets created to the route table.
5. Create a public route in the public route table created above with destination CIDR block 0.0.0.0/0 and internet gateway created above as the target.

## Cloud formation commands

1. Clone the repository

    ```sh
    git clone git@github.com:KetkiCloud6225/infrastructure.git
    ```


2. Run the following command to configure cli profiles
   
   ```
   aws configure --profile <profile-name>
   ```

3. Add the necessary ACCESS KEY ID , Secret ACCESS KEY

4. Run the following command to set a specific profile 

   ```
   export AWS_PROFILE=<profile-name>
   ```

5. Run this command to create cloud formation by specifying the yml file path

    ```
   aws cloudformation create-stack --stack-name stack-name --template-body file://csye6225-infra.yml
   ```

4. Run this command to delete the stack
    
    ```    
    aws cloudformation delete-stack --stack-name <stack-name>
    ```

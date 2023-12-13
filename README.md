
Point to note:-
Install terraform,awcli,aws configure by iam user or role update in ec2.
i did this project without a public key also.
ami id u can search in region under public ami ids filter.


Purpose of this Project:-

To create asg with vpc,subnet,route table,ig,route table association and install apache webserver onto ec2 created .


ssh-keygen is command to create keys 
and id_rsa.pub got created and the path i used below in variables.tf file:-


variables.tf code:-

variable "AWS_REGION" {
    default = "us-west-2"
}

variable "AMI" {
    type = map(string)

    default = {
        us-west-2 = "ami-0d593311db5abb72b"
        us-east-1 = "ami-0c2a1acae6667e438"
    }
}

variable "PUBLIC_KEY_PATH" {
    default =  "/home/ubuntu/.ssh/id_rsa.pub"
}


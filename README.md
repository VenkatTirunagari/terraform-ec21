mkdir terraform-ec2
cd terraform-ec2
touch provider.tf main.tf variables.tf outputs.tf .gitignore

main.tf
resource "aws_instance" "web" {
  ami           = "ami-0c02fb55956c7d316"
  instance_type = "t2.micro"

  tags = {
    Name = "Terraform-EC2"
  }
}

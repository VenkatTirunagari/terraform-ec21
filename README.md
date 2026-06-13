mkdir terraform-ec2
cd terraform-ec2
touch provider.tf main.tf variables.tf outputs.tf .gitignore

main.tf
resource "aws_instance" "web" {
  ami           = "ami-0b6d9d3d33ba97d99"
  instance_type = "t2.micro"

  tags = {
    Name = "Terraform-EC2"
  }
}

aws sts get-caller-identity

prowler

CIS BENCHMARK

aws ec2 describe-images --region us-east-1 --owner self --filter "Name=block-device-mapping.encrypted,Values=false" --query "Images[*].[ImageId]"
aws --region us-east-1 ec2 get-ebs-encryption-by-default
aws ec2 describe-volumes --filter Name=status,Values=available --query "Volumes[*].{ID:VolumeId}" --region us-east-1
aws ec2 describe-instances --region us-east-2 --output json --filters "Name=monitoring-state,Values=disabled" --query "Reservations[*].Instances[*].{Instance:InstanceId}"
aws ec2 describe-instances --region us-east-1 --output json --filters "Name=instance.group-name,Values=default" --query "Reservations[*].Instances[*].{Instance:InstanceId}"
aws ec2 describe-network-interfaces --region us-east-1 --output json --filters Name=status,Values=available --query "NetworkInterfaces[*].{ENI:NetworkInterfaceId}"
aws lambda list-functions --output table --query "Functions[*].FunctionName" --region us-east-1
aws lambda get-policy --function-name "prepaudit-prod-cron_difusion-343a" --output text --query "Policy" --region us-east-1
aws lambda get-function --function-name prepaudit-prod-procesamiento-imagenes-ecr-343a  --region us-east-1
aws s3 cp s3://343a-cf-resources/function/ . --recursive



Politica CONFIG

{
	“Version”: “2012-10-17",
	“Statement”: [
		{
			“Effect”: “Allow”,
			“Action”: “iam:PassRole”,
			“Resource”: “arn:aws:iam::239286574428:role/aws-service-role/config.amazonaws.com/AWSServiceRoleForConfig”
		},
		{
            “Effect”: “Allow”,
            “Action”: “config:StartConfigurationRecorder”,
            “Resource”: “*”
        }



 ![image](https://github.com/user-attachments/assets/26bff390-abb6-4532-ac21-ba3178b36284)



https://docs.cobalt.io/methodologies/cloud/

https://docs.cobalt.io/methodologies/cloud/


	]
}



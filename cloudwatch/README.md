### cli command 

> apply json with aws-cli


```bash
$ aws cloudwatch put-metric-alarm --cli-input-json file://[Path]/your_json_file_path.json
# sample 
# aws cloudwatch put-metric-alarm --cli-input-json file://home/.aws/cloudwatch_ec2_cpu.json
```

> not use json script

```bash 
# sample 
$ aws cloudwatch put-metric-alarm --alarm-name cpu-mon --alarm-description "Alarm when CPU exceeds 70%" --metric-name CPUUtilization --namespace AWS/EC2 --statistic Maximum --period 60 --threshold 50 --comparison-operator GreaterThanOrEqualToThreshold --dimensions  Name=InstanceId,Value=i-yourInstanceId --evaluation-periods 2 --alarm-actions arn:aws:sns:ap-northeast-2:728790254289:infra-warning-alarm --unit Percent
```
# Launching an EKS Cluster

https://github.com/ACloudGuru-Resources/Course_EKS-Basics


# create user and access key

```
aws iam create-user --user-name k8-admin

aws iam attach-user-policy \
    --policy-arn arn:aws:iam::aws:policy/AdministratorAccess \
    --user-name k8-admin

aws iam create-access-key \
    --user-name k8-admin
```

```
{
    "AccessKey": {
        "UserName": "k8-admin",
        "AccessKeyId": "AKIAU2HR67XXXXXXX",
        "Status": "Active",
        "SecretAccessKey": "FGb6lXCbKBXXXXXXXXXXXXXXXXX",
        "CreateDate": "2024-01-10T06:15:43+00:00"
    }
}
```

# Task 4: Cloud Security Implementation

## IAM (Identity and Access Management)
**Concept:** Controlling who can access what resources in the cloud.

**Example Policy:** 
- User: intern@company.com
- Permissions: Read-only access to storage
- Restrictions: Cannot delete or modify data

## Data Encryption
**Concept:** Protecting data by converting it into unreadable format.

**Types:**
- Encryption at rest (data stored)
- Encryption in transit (data moving)

## Security Policies Implementation:

### Sample IAM Policy for Intern:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Resource": [
        "arn:aws:s3:::codtech-bucket",
        "arn:aws:s3:::codtech-bucket/*"
      ]
    }
  ]
}
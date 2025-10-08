<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Justine Jurel Valenzuela  
**Email:** valenzuela.justinejurel@gmail.com

---

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use IAM (Identity and Access Management) to create and manage users, groups, and permissions in AWS. I’m doing this project to learn how to control access securely and manage user roles effectively.

### Tools and concepts

The services I used were EC2 and IAM. The key concepts I learned include launching an EC2 instance, creating user groups and users, setting up IAM policies, and using the IAM Policy Simulator to test those policies.

### Project reflection

This project took me approximately one hour to complete. The most challenging part was testing the instances, but the most rewarding part was seeing the IAM policies work as intended.

---

## Tags

Tags are labels you assign to AWS resources using key-value pairs. They are useful for organizing, identifying, and managing resources.

The tags I’ve used for my EC2 instances are “Name” and “Env.”
For the first instance, the tag values are Name: nextwork-dev-justinejurelvalenzuela and Env: development.
For the second instance, the tag value is Name: nextwork-prod-justinejurelvalenzuela and Env: production.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

IAM policies are rules that define what actions users or services are allowed or denied on AWS resources. They control who can access specific resources and what they can do with them, such as viewing, editing, or deleting.

### The policy I set up

For this project, I’ve set up a policy using JSON

I’ve created a policy that allows starting, stopping and describing EC2 instances with the tagged "Env = development" while denying the access to create and delete instances.

### When creating a JSON policy, you have to define its Effect, Action and Resource.

The Effect, Action, and Resource attributes in an IAM JSON policy define whether an action is allowed or denied, what specific actions can be performed, and on which AWS resources they apply. Together, they determine the level of access a user or service has.

---

## My JSON Policy

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_1c864649)

---

## Account Alias

An account alias is a user-friendly name that makes it easier to share and remember your AWS login URL, instead of using a long string of account ID numbers.

Creating an account alias took me 5 minutes. Now, my new AWS console sign-in URL is "https://nextwork-alias-justinejurelvalenzuela.signin.aws.amazon.com/console"

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### Users

IAM users are individual accounts in AWS that represent the people or applications and have a specific permission to access resources

### User Groups

IAM user groups are collections of users that allow us to manage permissions in one place, rather than assigning permissions to each user individually.

I attached the policy to the user group, so everyone in that group gets the same permissions from the policy.

---

## Logging in as an IAM User

The first way is to email the sign-in link and credentials directly to the user, and the second way is to download the .csv file containing the user’s credentials and share it securely.

Once I logged in as my IAM user, I saw some sections showing “Access Denied.” This is because the user doesn’t have permission to access those AWS services.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

I tested my JSON IAM policy by trying to stop both instances using the intern account. Only the development instance stopped successfully, while the production instance could not be stopped because the account doesn’t have permission to do so.

### Stopping the production instance

When I tried to stop the production instance, a pop-up message appeared saying I failed to stop it. This happened because the IAM policy only allows me to manage the development instance, not the production instance.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_0e7a9d6a)

---

## Testing IAM Policies

### Stopping the development instance

ChatGPT said:

Next, when I tried to stop the development instance, the request went through successfully, and the instance state changed to Stopped. This happened because the intern’s account has full access to the development instance.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_1811801c)

---

## The IAM Policy Simulator

The IAM Policy Simulator is used to test whether your IAM policies are working correctly. It’s a useful tool for safely verifying permissions without affecting real instances or disrupting other users.

### How I used the simulator

I set up a simulation for DeleteTags and StopInstances actions. Both were initially denied, so I adjusted the Env condition for StopInstances to development. After that, the simulation result changed to allowed.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-security-iam_069d8a621)

---

---

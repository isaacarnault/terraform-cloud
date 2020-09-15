Once you've complete the Get_Started section of this gist, you are ready to take this part.<br>

In this section, we will provision a `DynamoDB` instance through `Terraform Cloud`.

#### Step 1 - Configure AWS (must have an AWS account)

We will retrieve your `AWS` credentials and set your `Terraform Cloud` variables to use those values.

Log into your `AWS` account, if no account create one: https://portal.aws.amazon.com/billing/signup#/start.<br>
You can access your console after Signing Up to AWS using this link: https://console.aws.amazon.com/console/home.<br>

Once logged into your `AWS` console, go to `IAM`.<br>
If you are new to AWS, please bypass all user configuration (green ticked marks) for the sake of simplification.<br>

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-aws-1.png](https://i.postimg.cc/65HMJ3qg/isaac-arnault-aws-1.png)](https://postimg.cc/CzqGbwjs)

</p>
</details>

. Click on Users > Add user<br>

. Next: permissions > Create group: call it <b>admins_terraform</b>.<br>

. Filter policies: search for `AdministratorAccess` in the search bar.<br>

. Select the `AdministratorAccess` policy and click on 'Create group'.

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-aws-3.png](https://i.postimg.cc/jSwQp4Gn/isaac-arnault-aws-3.png)](https://postimg.cc/nXxD7BVn)

</p>
</details>

. Next: tags. Use as key: resources and as Value: terraform<br>

. Next: review > create user > download the .csv files which contains security credentials for the user '
terraform_user'<br>

`Access key ID` and a `Secret access key` were provided to you by `AWS`.<br>

Be sure to keep these values in a secure location; you will use them in the next step.<br>

You can keep this window opened and open a new `AWS` console window from your browser.

<hr>
<b>Important</b>
Follow `AWS` security best practices by deleting this user and the group created after completing this gist, since all security parameters for this user weren't fullfilled for the sake of simplicity.<br>


#### Step 2 - Configure workspace variables
Go back to your `Terraform Cloud` window and click on 'Configure variables'<br>

. Scroll down to `Terraform` variables > Add variables: here you'll create three (3) variables, one related to a user, and two related to the `DynamoDB` database: 'tag_user_name', 'db_write_capacity', 'db_read_capacity'.<br>

. Do the same for Environment variables > Ass variables: create 2 variables 'AWS_ACCESS_KEY_ID' and 'AWS_SECRET_ACCESS_KEY'.

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-aws-34.png](https://i.postimg.cc/wvZ0yb8z/isaac-arnault-aws-34.png)](https://postimg.cc/sQPpbmgH)

</p>
</details>

#### Step 3 - Queue and apply plan

. Click on Queue plan. When prompted, click on 'Confirm & Apply'.

<details>
<summary>🔴 See hint</summary>
<p>

[![isaac-arnault-terraform-34.png](https://i.postimg.cc/8kd6r0Vb/isaac-arnault-terraform-34.png)](https://postimg.cc/yWddMnxJ)

</p>
</details>

If everything is set up correctly, you should have this:

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-terraform-35.png](https://i.postimg.cc/mkVkpKLf/isaac-arnault-terraform-35.png)](https://postimg.cc/dZkJLHZ4)

</p>
</details>

If you get an error, make sure you've followed the prerequisites (Get_Started section of this gist) and that you've set the 5 requested variables correctly.<br>

You can go to your `AWS` console and check that the `DynamoDB` table was provisioned successfully.

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-terraform-38.png](https://i.postimg.cc/LXWpzWJ8/isaac-arnault-terraform-38.png)](https://postimg.cc/tZFwb2dK)

</p>
</details>

<hr>
At the end of this part you configured your workspace and provisioned a `DynamoDB` instance using `Terraform Cloud`. 

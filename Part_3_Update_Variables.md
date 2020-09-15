#### Step 1 - Change Infrastructure via Version Control

There are two (2) ways to update our workspace deployments on `Terraform Cloud`:<br>

- change the configuration in `VCS`.<br>
<b>or</b><br>
- update variables in the `Terraform Cloud UI.`

<hr>
<b>Important - </b> tools of our Workspace<br>

<b>Runs</b> - shows a list of all of the plan and apply actions you have taken with this workspace.<br>
<b>States</b> - shows a list of the entire tfstate file of your workspace after each successful run.<br>
<b>Variables</b> - let you configure Terraform variables and environment variables.<br>
<b>Settings</b> - contain all of the other configuration for your workspace.<br>
<b>Queue plan</b> - lets you start a new plan.
<hr>

#### Step 2 - Changing variables

In your `Terraform Cloud UI`, go to 'Variables'.<br>
You can try changing your 'db_read_capacity' value from 2 to 1.

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-terraform-37.png](https://i.postimg.cc/rptvhWVq/isaac-arnault-terraform-37.png)](https://postimg.cc/xknx8XNZ)

</p>
</details>

Click on 'Queue plan' and set as reason: 'db_read_capacity update'.

<details>
<summary>🔴 See hint</summary>
<p>
  
[![Screenshot-from-2020-09-12-18-49-53.jpg](https://i.postimg.cc/90cKFnGf/Screenshot-from-2020-09-12-18-49-53.jpg)](https://postimg.cc/BLwMmN7W)

</p>
</details>

You'll notice once queuing the plan that the log indicates that there are "0 to add, 1 to change, 0 to destroy", which corresponds to your update.

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-terraform-38.png](https://i.postimg.cc/QdFPt5Wc/isaac-arnault-terraform-38.png)](https://postimg.cc/Mn8t3n5G)

</p>
</details>
  
Then 'Confirm & update' and wait for the update confirmation:

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-terraform-40.png](https://i.postimg.cc/t48cVThw/isaac-arnault-terraform-40.png)](https://postimg.cc/Wd68BsYw)

</p>
</details> 

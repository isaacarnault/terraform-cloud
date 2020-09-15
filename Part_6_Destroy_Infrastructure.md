Destroying the infrastructure is part of `Terraform` normal workflow.

#### Destroy infrastructure

Go to your workspace in the `Terraform Cloud UI`.<br>
From the top menu select "Settings -> Destruction and Deletion".

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-terraform-31.png](https://i.postimg.cc/vH483thg/isaac-arnault-terraform-31.png)](https://postimg.cc/1fZZz6Ls)

</p>
</details>

. Queue destroy plan:

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-terraform-32.png](https://i.postimg.cc/g2vWTSZJ/isaac-arnault-terraform-32.png)](https://postimg.cc/685g7hzJ)

</p>
</details>

Confirm and apply when prompted and wait for the destruction:

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-33.png](https://i.postimg.cc/SsKbjmt2/isaac-arnault-33.png)](https://postimg.cc/yJ2bbCKs)

</p>
</details>

You'll notice that you've destroyed the plan but your workspace is still alive.

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-terraform-34.png](https://i.postimg.cc/FzdtgDvh/isaac-arnault-terraform-34.png)](https://postimg.cc/QK3njgVz)

</p>
</details>

Go back to 'Settings' and proceed to the workspace deletion.

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-terraform-35.png](https://i.postimg.cc/NfXqKJb4/isaac-arnault-terraform-35.png)](https://postimg.cc/KRmsV56k)

</p>
</details>

Confirm Workspace deletion when prompted and wait for the destruction.<br>

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-terraform-36.png](https://i.postimg.cc/KYZdsZbq/isaac-arnault-terraform-36.png)](https://postimg.cc/zyctyYVK)

</p>
</details>

In your Organization's workspace, you'll see that your `tf-guide-example` workspace was deleted.<br>

<details>
<summary>🔵 See output</summary>
<p>

[![Selection-061.png](https://i.postimg.cc/g0ZNDQXS/Selection-061.png)](https://postimg.cc/WDsGp97g)

</p>
</details>

<hr>
<b>Important</b><br>

Deleting a workspace does not destroy infrastructure that has been provisioned by that workspace. <br>

This means that your `AWS DynamoDB` table you provisioned isn't destroyed after destroying the plan and infrastructure on `Terraform Cloud`.<br>

Mitigating the cost of the Infrastructure, especially if you are a `Data Architect` / `Solution Architect` is quite important. <br>

Please bear in mind that running costs may occure if you do not delete the resources provided by your `Terraform` actions.<br>

<hr>

Thus, feel free to go to your `AWS` console and delete the User, Group, DynamoDB table created upon this gist completion.

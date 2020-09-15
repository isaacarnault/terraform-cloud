Taking part 5 is not mandatory.<br>

But if we want to take advantage of your 'Try out the Team & Governance plan features for 30 days' plan, we can set a Sentinel policy and a new Policy set to our forked 'tfc-guide-example' repository.<br>

#### Step 1 - Create a new Sentinel Policy and Policy Set

We connect to our Terraform Cloud UI, click on Settings, click on Policy Sets.<br>

Now we will add a new Sentinel Policy. Click on Policies.<br>

Create a new policy > call it 'tfc-guide-example-sentinel-policy'<br>

Description (not compulsory): 'First sentinel policy'.<br>

Enforcement mode: choose 'Soft-mandatory'<br>

Policy code: add the following line of code<br>

```r
main = rule {
	true
}
```
click on 'Create your first policy set' > connect to GitHub > Choose a repository: choose 'tfc-guide-example'

<details>
<summary>🔴 See hint</summary>
<p>
  
[![isaac-arnault-terraform-31.jpg](https://i.postimg.cc/T1jgdkTC/isaac-arnault-terraform-31.jpg)](https://postimg.cc/YL9h8zGW)

</p>
</details>

Scope of policies > select 'Policies enforced on selected workspaces'.<br>

In the Workspaces box, select 'tfc-guide-example' workspace, then 'Add workspace'.

Next: click on 'connect policy set'<br>

<details>
<summary>🔴 See hint</summary>
<p>

[![isaac-arnault-terraform-50.png](https://i.postimg.cc/XYVrPMDH/isaac-arnault-terraform-50.png)](https://postimg.cc/vcN81Kyf)

</p>
</details>

#### Update GitHub repository

Now that we have a new Sentinel policy and a Policy Set, we should add one file into our GitHub repository otherwise we'll get some error while queueing our plan.<br>

We go to 'tfc-guide-example' repository that we've forked.<br>

Click on 'Add file' > 'Create new file'

<details>
<summary>🔴 See hint</summary>
<p>

[![isaac-arnault-terraform-53.jpg](https://i.postimg.cc/PJ2grwT8/isaac-arnault-terraform-53.jpg)](https://postimg.cc/N22JdLyg)

</p>
</details>

Call the file 'allowed-terraform-version.sentinel' and pass the following code onto it then click on 'Commit'<br>

```r
main = rule {
	true
}
```
Our newly created file should look like this:

<hr>
[![isaac-arnault-terraform-54.png](https://i.postimg.cc/4N3C2BQv/isaac-arnault-terraform-54.png)](https://postimg.cc/jCBkL69C)
<hr>

<hr>
At this part of the turorial, we have one Sentinel policy and one Policy Set configured as well as a new file created on our GitHub repository.<br>
We are now ready to run a new 'Queue plan'
<hr>

#### Step 2 - Queue plan to apply your policies

We go to our 'tfc-guide-example' workspace and click on 'Queue plan'.<br>

Upon completion, a new tab 'Policy check' should appear in our UI.<br>

If we have properly configured our Sentinel policy and Policy Set as well as our repository file, Policy check should pass.

<hr>

[![isaac-arnault-terraform-55.png](https://i.postimg.cc/qqMFYvyB/isaac-arnault-terraform-55.png)](https://postimg.cc/47qwHZWj)

<hr>

This gist is now completed. We have successfully completed part 1 to 6.

<hr>

[![isaac-arnault-terraform-56.png](https://i.postimg.cc/ncr5GMn0/isaac-arnault-terraform-56.png)](https://postimg.cc/mtx8bLzH)

<hr>

We have successfuly implement an Infrastructure as Code using Terraform Cloud, GitHub and AWS which helped us provision a DynamoDB table.<br>
If you enjoyed this gist, thanks for forking it and do not hesitate to raise questions.

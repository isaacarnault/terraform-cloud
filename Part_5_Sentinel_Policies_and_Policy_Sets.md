Doing part 5 is not mandatory.<br>

But if we want to take advantage of your `Team & Governance plan` trial plan, we can set a Sentinel policy and a new Policy set.

<hr>

#### Step 1 - Create a new Sentinel Policy and Policy Set

We connect to our `Terraform Cloud UI`, click on <b>Settings</b>, click on <b>Policy Sets</b>.<br>

Now we will add a new `Sentinel Policy`. Click on <b>Policies</b>.<br>

Create a new policy > call it `tfc-guide-example-sentinel-policy`<br>

Description (not compulsory): 'First sentinel policy'.<br>

Enforcement mode: choose <b>Soft-mandatory</b><br>

Policy code: add the following line of code<br>

```r
main = rule {
	true
}
```
- click on <b>Create your first policy set</b>
- connect to GitHub
- choose a repository: choose <b>tfc-guide-example</b>

<details>
<summary>🔴 See hint</summary>
<p>
  
[![isaac-arnault-terraform-31.jpg](https://i.postimg.cc/T1jgdkTC/isaac-arnault-terraform-31.jpg)](https://postimg.cc/YL9h8zGW)

</p>
</details>

Scope of policies > select <b>Policies enforced on selected workspaces</b>.<br>

In the Workspaces box, select <b>tfc-guide-example</b> workspace, then <b>Add workspace</b>.

Next: click on <b>connect policy set</b><br>

<details>
<summary>🔴 See hint</summary>
<p>

[![isaac-arnault-terraform-50.png](https://i.postimg.cc/XYVrPMDH/isaac-arnault-terraform-50.png)](https://postimg.cc/vcN81Kyf)

</p>
</details>

<hr>

#### Step 2 - Update GitHub repository

Now that we have a new `Sentinel policy` and a `Policy Set`, we should add one file into our GitHub repository otherwise we'll get some error while queueing our plan.<br>

We go to <b>tfc-guide-example</b> repository that we've forked.<br>

Click on <b>Add file</b>, then <b>Create new file</b>

<details>
<summary>🔴 See hint</summary>
<p>

[![isaac-arnault-terraform-53.jpg](https://i.postimg.cc/PJ2grwT8/isaac-arnault-terraform-53.jpg)](https://postimg.cc/N22JdLyg)

</p>
</details>

Call the file <b>allowed-terraform-version.sentinel</b> and pass the following code onto it, then click on <b>Commit</b><br>

```r
main = rule {
	true
}
```

Our newly created file should look like this:

<details>
<summary>🔵 See output</summary>
<p>
	
[![isaac-arnault-terraform-57.png](https://i.postimg.cc/tg6j4CrC/isaac-arnault-terraform-57.png)](https://postimg.cc/mcTqdRf0)

</p>
</details>

We have one `Sentinel policy` and one `Policy Set` configured as well as a new file created in our `GitHub` repository.<br>

We are now ready to run a 'Queue plan'.

<hr>

#### Step 3 - Queue plan to apply your policies

We go to our <b>tfc-guide-example</b> workspace and click on 'Queue plan'.<br>

Upon completion, a new tab `Policy check` should appear in our UI.<br>

If we have properly configured our `Sentinel policy` and `Policy Set` as well as our repository file, `Policy check` should pass.

<hr>

[![isaac-arnault-terraform-55.png](https://i.postimg.cc/qqMFYvyB/isaac-arnault-terraform-55.png)](https://postimg.cc/47qwHZWj)

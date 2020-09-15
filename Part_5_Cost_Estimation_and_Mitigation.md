Estimating and mitigating costs of your deployed resources via `Terraform Cloud` can useful in your job.<br>

#### Prerequisites
In order to get cost estimation of your deployed resources upon `Queue plan`, make sure you move from a free plan to a paid plan.<br>

On the top bar click on Settings > Plan & Billing.<br>

Choose the Team & Governance free trial plan to try new `Terraform Cloud` tools for free (30 days free trial).<br>

[![isaac-arnault-terraform-51.png](https://i.postimg.cc/MphrnyXk/isaac-arnault-terraform-51.png)](https://postimg.cc/18rKTVpM)

Now that you've switched to a paid plan, you'll see that new tabs appeared in your left sidebar such as `Cost Estimation`, `Policy Sets`. <br>

Click on `Cost Estimation` and make sure that <b>Enable Cost Estimation for all workspaces</b> is checked.

<details>
<summary>🔵 See output</summary>
<p>

[![isaac-arnault-terraform-52.png](https://i.postimg.cc/15XWMWqh/isaac-arnault-terraform-52.png)](https://postimg.cc/Tp8q3J0C)

</p>
</details>

Now we are ready to go!

#### Infrastructure cost mitigation using Terraform Cloud UI

Let's go back to our Terraform Cloud UI on ou <b>tfc-guide-example</b> workspace to add new parameters.<b>
  
Go to `Terraform variables`.<br>

Add 1 new variable: `aws_region` and set <b>us-west-1</b> as value.<br>

Update your `db_read_capacity` to <b>2</b>.

<details>
<summary>🔴 See hint</summary>
<p>

[![isaac-arnault-terraform-53.png](https://i.postimg.cc/mDcNfrQb/isaac-arnault-terraform-53.png)](https://postimg.cc/cgS8f09j)

</p>
</details>

Then click on `Queue plan`.<br>
Applying our new plan will unlock a new `Cost estimation` feature in our UI.

[![isaac-arnault-terraform-54.png](https://i.postimg.cc/YqBNZMjH/isaac-arnault-terraform-54.png)](https://postimg.cc/0rZJJgpW)

By clicking on the `Cost estimation` tab we can see the Hourly, Monthly and Monthly Delta costs of our `DynamoDB` table deployed on `AWS`.<br>

[![isaac-arnault-aws-55.png](https://i.postimg.cc/dtRRKpTT/isaac-arnault-aws-55.png)](https://postimg.cc/Vd60q7gY)

Finally, let's confirm that our `DynamoDB` was deployed on `AWS`:<br>
- Log into our `AWS` console.<br>
- Switch to `us-west-1` region.<br>
- Open `DynamoDB` service.

Here is our table!

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-aws-56.png](https://i.postimg.cc/fWmmxpCg/isaac-arnault-aws-56.png)](https://postimg.cc/WtpdV9QM)

</p>
</details>

To mitigate your costs, do not forget to delete the `DynamoDB` table created upon this part completion, directly throughout your `AWS` console.

<details>
<summary>🔵 See output</summary>
<p>
  
[![isaac-arnault-terraform-55.png](https://i.postimg.cc/vBL8mr7X/isaac-arnault-terraform-55.png)](https://postimg.cc/wyMYfsGs)  

</p>
</details>

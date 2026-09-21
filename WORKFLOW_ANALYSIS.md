**What triggers this workflow to run? (Look at the on: section)**

The workflow runs when code is pushed to the main branch which is the conventional way or when a pull request is opened/updated for the main branch.

**What are the four main steps this workflow performs? (List each step name)**

- Checkout code 
- Validate HTML
- Check links
- Upload artifact

*if those succeed, the deploy job performs deploy to Github Pages.*

**What does the "Checkout code" step do and why is it necessary?**

It copies the repositories code onto the Github Actions runner and this is necessary because the entire workflow needs access to the project files before it can prepare the website for deployment.

**What is the purpose of the environment configuration?**

It tells GitHub that the deployment is going to the GitHub Pages environment; it also helps GitHub know where the website if published. 

**How does this automated deployment improve reliability compared to manual deployment?**

It reduces the chance of accidentally publishing broken code or forgetting a deployment step which is crucial for the depolyment of websites something that I think is incredibly useful in world-wide developement.

**What would happen if you pushed code to a different branch (not main)?**

It would not trigger a workflow because the push trigger feature is only configured for main but if that branch was used to create a pull request into main the workflow would still run. 
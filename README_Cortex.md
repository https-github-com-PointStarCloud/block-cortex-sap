<h1><span style="color:#2d7eea">Google Cloud Cortex Framework for SAP</span></h1>

Gain faster insights into your Order to Cash, Finance, and Inventory data with these Dashboards and Explores based on the [Google Cloud Cortex Framework](https://cloud.google.com/solutions/cortex#google-cloud-cortex-framework) for SAP. Leverage or customize this Looker model to:
* Identify trends and patterns in your data
* Spot potential problems early on
* Make better decisions faster

For detailed information including content and installation instructions, checkout the dedicated Looker Block for SAP [documentation](https://cloud.google.com/cortex/docs/looker-block-sap).

## Deployment Steps
### Prerequisite
- [Deploy Cortex Framework](https://github.com/https-github-com-PointStarCloud/cortex-data-foundation)
- [Looker Access](https://pointstar.cloud.looker.com/login)
### Installation
- Option 1: [Install by forking the repository.](https://cloud.google.com/cortex/docs/looker-block-deployment#option_b_install_by_forking_the_repository). Use clone instead of fork to ensure the repository remains private
- Option 2: [Install through Looker Marketplace from a Git URL](https://cloud.google.com/cortex/docs/looker-block-deployment#install-through-Looker-marketplace-from-a-git-url)
Option 1 is preferred as it provides version control. It can be summed up as follows:
1. Setup GitHub repository
2. Create blank LookML project
3. Setting up connection between LookML project and git using SSH
4. Updating `manifest.lkml` for setting up LookML configuration 
5. Update marketplace.json which will be used to deploy marketplace.json
6. [Configure additional spec for deployment where necessary](https://cloud.google.com/cortex/docs/looker-block-sap#additional_specifications_for_deployment)
7. Commit and deploy changes to production
8. Use Option 2 to deploy the dashboard to Block  
## Managing Cortex Block SAP
The approach here works similar with cortex-data-foundation github. Clone for setting up private repository and fetch for maintaining them
### Setting Up Private Repository
- clone google cloud sap block cortex repository
- push to pointstar sap block cortex repository
- pointstar will have 1 repository, `pointstar-main` (latest from Google and updated by PointStar)
### Updating Private Repository 
- fetch updates from google cloud sap block cortex repository
- merge those updates to local pointstar-main
- push them to remote local pointstar-main 
### Setting Up Customer Repository
- make new repository based on the private repository
- make 3 repositories which are `development`, `pre-production`, `production`
### Updating Customer Repository
- make `feature` branch by copying from development 
- fetch updates from google cloud sap block cortex repository
- merge those updates to local pointstar-main
- resolve conflict and push to remote customer repositories
### NOTES : 
 - Git provider : GitHub, GitLab, BitBucket, AWS CodeCommit etc.
 - GitOps : using Git everywhere from development to deployment. 
 - Wikimedia (org.) -> Mediawiki (soft./CMS) -> Wiki's (web apps) -> wikipedia (most popular app/product)
	 - No Code/Low Code/CMS (Wordpress, drupal, mediawiki-Customwiki)/Headless CMS
	 - **CMS -> Headless CMS -> SSG -> SSR**
	   - CMS - Wordpress, Magento
	   - Headless CMS - Strapi, netlify cms, wordpress headless, Ghost, sanity etc. (Headless DB, Ecommerce etc.)
	   - Static Site Generators(SSG) - Gatsby, Hugo, Jekyll, Eleventy, React Static, Gitbook, Sveletekit
	   - Server side Renderer (SSR supports SSG) - Next, Nuxt, Quasar etc.

 - Domain is name address to IP (DNS server), whereas hosting is Cloud server (web,email,etc.)
 - State : Stateless, state-full (HTTP, TCP, Websockets)
 - OS/Compute Env./CPU/VM/remote Workspace : Linux/MacOS/Windows (Intel/ARM/AMD)
 - Remote administration
	 - Remote Access/Conn. via :
		 - Protocols : RDP, RFB/VNC, WOL/Wake-on-LAN, X11, etc.
		 - VPN/Tunneling/PPP (Terminal Emulation) : SSH (keygen), Telnet (Old), FTP etc. [Terms : NAT/proxy/port fwd]
		 - Other Unconventional ways (web based) : HTTP/S, Peer2Peer (level.io)
	 - Softwares : Teamviewer, anydesk, Tight/RealVNC, Chrome remote (web/mobile), SSH (cygwin/putty/openssh, SecureCRT, winSCP) etc.
 
 ---
 ### Deployment (DevOps/CI-CD) : 
  - **Scalablity :** 
	  - Horizontal (Adding resources)
	  - Vertical (increasing capacity of current resources)
  - **CI/CD Tools :** 
	  - GitOps : Gitlab CI/CD, Github Actions etc. [K8's based & Directly packaged all in one | Other - Azure DevOps]
	  - IaC (Infra. as code - provisioning or creating infra./server via code) : 
		  - Dev. - Terraform (Hashicorp), AWS CloudFormation
		  - Deployment (Custom) - Travis CI, Circle CI, Jenkins, Ansible, Chef, Puppet, Saltstack etc.
	  - Others : Codeship, Fabric8 etc.
  - **Models** : 
	  - **Pull**/Client Pull -  Server to be configured will pull its config. from the controlling server. Eg. Chef, Puppet, Gitops etc.
	  - **Push**/Server Push - Controlling server pushes config. to destination system. Eg. Anisble, Terraform, Jenkins, CircleCI, TravisCI etc.
	  - Hybrid (Push & Pull) - Saltstack etc.
  - **Strategies** : 
	  - All at once (deploy_in_place/Recreate deployment)
	  - Blue/green or red/black
	  - Canary
	  - Rolling/Ramped
	  - Shadow Deployment
	  - A/B Testing Deployment
	  - Others - Dark launch deployments, Hot Deployments, Partial Deployments etc.
  - **Different ways to deploy web apps** : [Self-hosted/IaaS -> PaaS/SaaS -> Container/Docker/Kubernetes/serverless-FaaS -> Hybrid-Container+serverless]
	  - **Traditional** : Manually copy/pasting code (ftp) on prod server and config it.
	  - **IaaS** : deploy web app (git) on self-host/custom/DIY Server/OS & Config it via SSH - VPS (GCE, AWZ EC2, Azure VM, Vultr, Linode etc.)
	  - **PaaS (devops/gitops) :** Deploy automatically on git push Trigger on PaaS (Heroku, Vercel, Netlify etc.) **OR** {All in one Pckg. - Github Actions/Gitlab CI-CD/Azure devops} **OR** GCP(app engine), AWS(elastic beanstalk,amplify,lightsail) Azure(app service)
	  - **SaaS+FaaS (devops/gitops) :** Deploy via SaaS/Container/Docker/K8/GKE-GCE/AKE-ACE/ECS-EKS **OR** SaaS+Serverles/FaaS (On-premise/self-hosted - google cloud run, ACI, AWS App runner)
	  - **NOTE (5 ways)** : In Short, Either do it manually(ftp/ssh) either on your own server/cloud-IaaS **OR** Deploy via PaaS(Vercel)/Devops Package (Actions/Gitlab CI-CD)/Cloud Solutions(App engine,beanstalk) **OR** Via container services **OR** Serverless/FaaS services **OR** Container+FaaS (Cloud run)
  - **Devops pipeline & Dev. env.**
	  - **NOTE** : 
		  - Sandbox could be dev/test/pre-pod env.
		  - **Devops Pipeline :** Commit -> Build -> Unit Test -> Merge to trunk/main -> Integ. test -> Staging -> Reg. test -> Deploy
		  - **Dev. env. workflow** : Dev -> Test/QA -> Staging/UAT/demo/pre-pod/snapshot/model -> Prod/live
	  - **Continuous Integration (CI) :** Commit + Build + Test
		  - **Development** (Gitflow/Gitops - Dev/Feature/hotfix branch)
		  - **Testing** (Gitflow/Gitops - Test/support branch)
	  - **Continuous Delivery (CD) :** CI + Release/PrePod (Manual Deployment)
		  - **Staging** (Gitflow/Gitops - Release branch)
	  - **Continuous Deployment (CD) :** Cont. Delivery + Deploy/Prod (Everything Same except auto deployment)
		  - **Production** (Gitflow/Gitops - Main or Master branch)

![Github-Actions](img/Github%20Actions%20CI%20CD%20Devops.png)
![Gitlab-CI-CD](img/gitlab%20CI%20CD%20Devops%20pipeline%20workflow.png)

---

### Cloud [GCP, AWS, Azure] : IaaS/VM/HW/Servers -> PaaS/OS/DB -> SaaS/SW/Container-docker-K8's ~ FaaS/Serverless
- **IaaS :** AWS EC2, Goole GCE, Azure VM, Digital Ocean, Linode, Rackspace, Vultr, Render.com etc.
- **PaaS (Deployment) :** Heroku | Netlify | Vercel | Github Pages | Google App Engine | Azure App Service, Container Apps | AWS Elastic Beanstalk, Lightsail | Engine Yard | JAMStack | Dokku (Digital Ocean) | Fly.io | pythonanywhere | Railway | Cyclic.sh | Surge.sh
- **SaaS/Containers :** Google Drive, dropbox, GKE/GCE, AKE/ACE, ECS/EKS etc.
- **FaaS/Serverless :** AWS Lambda, Azure function, google cloud function
- **SaaS+FaaS (Best of all) :** Google Cloud Run, AWS App Runner, Azure Container Instances(ACI)
- **Other :** 
	- **M/BaaS (Auto API's : Rest/Graphql) :** Firebase | Hasura | AWS Amplify | Prisma | Back4Ap | Parse
	- **DBaaS (Online DB) :** Airtable | MongoDB Atlas | ElephantSQL(PostgreSQL) | YugaByteDB | Cockroachlabs | redislabs | Astra(Cassandra) | Notion(PM) | G Sheets | Navisite (mySQL as service) | ElasticCloud | Google CloudSQL, Cloud Firestore | AWS DynamoDB, RDS | Azure MS SQL Server, CosmoDB, DocumentDB

---

### Cloud IDE (Remote dev. env.)  :
- **Type 0 :** Web editor/playgrounds/sandbox workspaces (Codepen, JSFiddle, JSBin, Codeply etc.)
- **Type 1 :** Client side compute (Stackblitz, Codesandbox, webcomponents.dev etc.)
- **Type 2 :** Thin client & server side compute [Company's server/SaaS] (Codedamn, repl.it, Glitch, etc.)
- **Type 3 (DIY Cloud IDE) :** Thin client (VScode/other IDE is dumped at frontend) & server side compute [Company's server/SaaS OR Self-hosted DIY Server]
	- **SaaS :** VS Code Remote (remote-ssh/WSL, Github Codespace (SaaS), dev container), Google Cloud code, gitlab web IDE, Eclipse Theia/Che, Redhat openshift/codenvy, goorm, Cloud9 (Custom IDE/AWS EC2), codeanywhere, sourcelair, PaizaCloud, shiftedit, codetasty etc.
	- **SaaS + DIY/Self-hosted :** Coder.com/Code-Server, GitPod (vscode ide), koding etc.

---


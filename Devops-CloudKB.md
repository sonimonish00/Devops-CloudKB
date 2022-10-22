### NOTES : 
 - Git provider : GitHub, GitLab, BitBucket, AWS CodeCommit etc.
 - GitOps : using Git everywhere from development to deployment. 
 - Wikimedia (org.) -> Mediawiki (soft./CMS) -> Wiki's (web apps) -> wikipedia (most popular app/product)
	 - No Code/Low Code/CMS (Wordpress, drupal, mediawiki-Customwiki)/Headless CMS
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
	  - GitOps : Gitlab CI/CD, Github Actions etc. [K8's based]
	  - IaC (Infra. as code) : 
		  - Dev. - Terraform (Hashicorp), AWS CloudFormation
		  - Deployment - Travis CI, Circle CI, Jenkins, Ansible, Chef, Puppet, Saltstack etc.
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
  - **Different ways to deploy** : [Self hosted VPS/IaaS -> PaaS -> Container/Docker/Kubernetes -> Container+serverless/Google Cloud run]
	  - **Traditional** : Manually copy/pasting code (ftp) on prod server and config it.
	  - **IaaS** : deploy web app (git) on self-host/custom/DIY Server/OS & Config it via SSH - VPS (GCP,AWZ,Azure,Vultr,Linode etc.)
	  - **PaaS** : Deploy automatically on git push Trigger (Actions/CI-CD/yaml/hooks) on PaaS (Heroku, Vercel, Netlify etc.)
	  - **SaaS+FaaS (GitOps) :** Deploy via Contanerized Cluster/Docker/K8 (SaaS) or SaaS + serverless (FaaS)(On-premise/self-hosted)
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
- **IaaS :** Digital Ocean, Linode, Rackspace, AWS EC2, GCE, Azure, Vultr, Render.com etc.
- **PaaS (Deployment) :** Heroku | Netlify | Vercel | Github Pages/surge.sh | Google App Engine | Azure App Service | AWS Elastic Beanstalk | Engine Yard | JAMStack | Dokku (Digital Ocean) | Fly.io | pythonanywhere | Railway | AWS Elastic Beanstalk | Cyclic.sh
- **SaaS/Containers :** Code-server, GitPod, Google Drive, Google Cloud Code, Codespace, cloud9, dropbox etc.
- **FaaS/Serverless :** AWS Lambda
- **SaaS+FaaS (Best of all) :** Google Cloud Run
- **Other :** 
	- **M/BaaS (Auto API's : Rest/graphql) :** Firebase | Hasura
	- **DBaaS (Online DB) :** Airtable | MongoDB Atlas | ElephantSQL | YugaByteDB | Cockroachlabs | redislabs | Astra | Notion(PM) | G Sheets

---

### Cloud IDE (Remote dev. env.)  :
- **Type 0 :** Web editor/playgrounds/sandbox workspaces (Codepen, JSFiddle, JSBin, Codeply etc.)
- **Type 1 :** Client side compute (Stackblitz, Codesandbox, webcomponents.dev etc.)
- **Type 2 :** Thin client & server side compute [Company's server/SaaS] (Codedamn, repl.it, Glitch, etc.)
- **Type 3 (DIY Cloud IDE) :** Thin client (VScode/other IDE is dumped at frontend) & server side compute [Company's server/SaaS OR Self-hosted DIY Server]
	- **SaaS :** VS Code Remote (remote-ssh/WSL, Github Codespace (SaaS), dev container), Google Cloud code, gitlab web IDE, Eclipse Theia/Che, Redhat openshift/codenvy, goorm, Cloud9 (Custom IDE/AWS EC2), codeanywhere, sourcelair, PaizaCloud, shiftedit, codetasty etc.
	- **SaaS + DIY/Self-hosted :** Coder.com/Code-Server, GitPod (vscode ide), koding etc.

---


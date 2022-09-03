# Module 2: DevOps Methodology

## DevOps Culture

- Highly collaborative environment: whole team has end-to-end ownership for released software
  - Work together to optimize productivity of developers and reliability of operations
  - Enables process to be unified and continuously improve to deliver on business goals
- Automate When Possible: enable teams to focus on innovation by automating repeatable tasks
  - Provides means to rapid development, testing, and deployment
  - Identify automation opportunities at every stage (e.g. code integrations, review, testing, security, deployments, and monitoring, and using right tools and services)
- Focus on Customer Needs: Feedback loops within DevOps teams means that customer feedback reaches development phase sooner
  - With microservices architecture, able to quickly switch direction and align efforts with required needs
- Develop Small and Release Often: applications should be designed with smaller, loosely couple components
  - Overarching policies are in place to provide governance to development efforts
- Include Security at Every Phase: security must be iterative, incremental, automated, and in every phase of application lifecycle
  - Educate development and operations teams to embed security into each step
- Continuously Experiment and Learn: leadership accepts failure and teams are encouraged to see failure as a learning opportunity
- Continuously Improve: thoughtful metrics help teams monitor progress, evaluate processes and tools, and work toward common goals and continuous improvement

## DevOps Practices

- Communication and Collaboration: facilitate feedbacks for good communication and collaboration within teams
- Monitoring and Observability: help teams react, learn, plan, and improve
  - Consolidate and visualize data gathered by an observable system over time so that teams gain insight on performance, identify trends, can set alarms, and make predictions on expected outcomes
- Continuous Integration (CI): developers regularly merge their code changes into a central repository, after which automated builds and tests are run
  - Teams can resolve merging issues and code defects early when they are easier and more cost effective to resolve
  - Key goals: find and address bugs quicker, improve software quality, and reduce the time it takes to validate and release new software updates
- Continuous delivery/deployment (CD): softare development practice where every code change is automatically built, tested, and then deployed to non-production testing or staging environment
  - Manual approval is required before pushing to production
  - Developers will always have a deployment-ready build artifact that has passed through a standardized test process
- Microservices: builds an application as a set of loosely coupled services
  - Type of architecture teams settle on is a direct predictor of how successful they will be with achieving continuous delivery
- Infrastructure as Code (IaC): practice in which infrastructure is provisioned and managed using code and software development techniques (e.g. version control and continuous integration)
  - Cloud API-driven models (e.g. Terraform) enable developers and system administrators to interact with infrastructure programmatically and at scale
- DevOps (CI/CD) pipeline: set of stages that move code from source to deployment
  - Code: develop code in a language and deliver to a central location (branch)
  - Build: perform actions on submitted code (e.g. compile, check code styles/standards, analyze complexity and maintainability of code, validate dependencies, create container images, and run unit tests)
  - Test: assess if application meets defined requirements (e.g. functional testing, integration testing, regression testing, acceptance testing, load testing, security testing)
  - Release: prepare and package tested code with specific version number
  - Deploy: release to targeted environment (e.g. test, staging, alpha, beta, or production)
  - Monitor: quickly detect unusual activity or errors

## DevOps Tools

- Cloud: provision environments on demand for building, testing, and/or experimenting
- Development: IDEs, SDKs, and VCSs
- CI/CD: build, source control, deployment, and pipeline automation tools
  - Automate continuously integrated code that teams develop, check compliance with standards, run testing more frequently, promote code to different test environments, and deploy products to infrastructure
- Infrastructure Automation: programmatically define your infrastructure, including constraints, to repeatedly and consistently provision your environments
- Containers and Serverless: enable developers to focus on applications and not the details of the host environment
- Monitoring and observability are key aspects in being proactive in preventing challenges before they occur

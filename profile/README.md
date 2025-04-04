# PAYRIT
### Experience the fastest way to go global with your money

![Logo](images/IMG_0899.PNG)

#### HIGHLEVEL ARCHITECTURE DIAGRAM
![HLAD](images/HLAD.png)

#### Pay globally with local currency flow
![FLOW](images/flow.png)

#### Pay globally with local currency flow on stellar blockchain
[FLOW ON EXCALIDRAW](https://excalidraw.com/#json=gMe5LnYUQ4r6NNo7DSbtw,eZzZT2yJkdwxBOp2rlWMXg)

## 1. Backend system Component 
- **Client Application** : Mobile (IOS, ANDROID) and Rest API for integration with other products we provide services to. 
- **Backend Service** : Microservice architecture 
    - Payrit core system : Typescript,  NEST JS, 
    - Database: MongoDB, Redis, 
    - Messaging layer: Bull Mq, Kafka
    - Crypto service: Java, Spring boot
    - NGN provider: Anchor(BaaS)
    - Cyrpto/Cross border Provider/: Stellar Network

- **Deployment and Infrastructure**: 
  - Our system leverages robust AWS services and additional tools to ensure scalability, reliability, and ease of management across multiple isolated environments.

    - Infrastructure Overview:
       - AWS Services:

        - Elastic Beanstalk: Simplifies the deployment and scaling of our backend services.
        - EC2: Provides scalable compute capacity for our applications.
        - Elastic Cache: Ensures low-latency data access and caching.
        - AWS CodePipeline: Automates our CI/CD workflows for seamless deployment.
        - Amazon MSK: Manages our Kafka workloads for efficient data streaming.
        - Horizon: Plan to Host as Docker containers on Amazon  EKS (Elastic Kubernetes Service), ensuring container orchestration and scalability.
        Dedicated Private Cloud (Backup):

        - A dedicated on-premises server connected to the internet using Ngrok.
            #### Functions: 
            - Serves as a backup environment for pre-production testing.
            - Acts as a fallback during system upgrades to ensure continuity.
        - Cloudflare:

           - Hosts our websites, provides a Web Application Firewall (WAF), and maps subdomains to their respective environments for better traffic management.

- **Monitoring**: 

    We have integrated Datadog tracing to:
    - Visualize the connections and dependencies between all services.
    - Identify and troubleshoot errors quickly.
    - Enhance system observability, improving overall operational efficiency.


## 2. Integration with Stellar
- Utilizing Stellar network, we offer user a blockchain wallet for supported assets starting with XLM and USDC
- Cross border payment:
    - Path Payments: Allows us to implement our "*spend in any country using your local currency*"
        - We would implement path payment strict Receive for this feature, because the goal is pay in any currency while trader, merchants get the real value for their goods or services

    - Stellar Anchor: We have integration with some of the anchors on stellar's anchor directory such as flutterwave and we will integrate with more of them.
    They will be help us collect funds in user's local currency and help deliver it to the destination asset/currency

- Enhancing our scan-to-pay and NFC feature
    - We currently operate in the local space in Nigeria. we started payrit with the initial goal of bridging the gap between the banked and the unbanked. This feature has been in our users' hand and it has allowed them to pay in rural settings where user need to sort for cash to pay the traders. With stellar integration we can now enhance this feature to allow user still use the scan-to-pay feature but debiting their crypto or alternate wallets

## 3. Compliance and Security
- As at today Payrit has one of this srictest and fastest hybrid KYC verification process. we combined but automatical KYC verification by leveraging one of africa's leading KYC verification service. We have an internal dashboard to manually approve the KYC and move user to the next KYC level. 
We are doing this because we understand we operate in a delicate and vulnerable industry prone to fraud and Money laundry, Hence our hybrid approach in order to give the human touch in verifying users.
We have built an internal system that notifies the payrit's admins when there is a new kYC verification request.

- We partnered with banking services that are licensed and are a member of the [NDIC](https://ndic.gov.ng/) to secure our user's funds.

- We have plan to bring onboard cyber security expert to helps improve the security of all our services


-----------



---------

### *We are dedicated to empowering Africans by providing them with the opportunity to seamlessly participate in the global financial ecosystem.*

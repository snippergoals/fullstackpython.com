title: Serverless
category: page
slug: serverless
sortorder: 0538
toc: False
sidebartitle: Serverless
meta: Serverless is an deployment architecture where servers are not explicitly provisioned and code is run based on pre-defined events.


# Serverless
Serverless is a [deployment](/deployment.html) architecture where 
[servers](/servers.html) are not explicitly provisioned by the deployer. 
Code is instead executed based on developer-defined events that are 
triggered, for example when an HTTP POST request is sent to an 
[API](/application-programming-interfaces.html) a new line written to a file.


## How can code be executed "without" servers?
Servers still exist to execute the code but they are abstracted away from 
the developer and handled by a compute platform such as 
[Amazon Web Services Lambda](/aws-lambda.html) or 
[Google Cloud Functions](/google-cloud-functions.html).

<img src="/img/visuals/serverless.png" width="100%" alt="Serverless compute spectrum." class="technical-diagram"> 

Think about deploying code as a spectrum, where on one side you build your
own server from components, hook it up to the internet with a static IP
address, connect the IP address to DNS and start serving requests. The 
hardware, operating system, web server, WSGI server, etc are all completely 
controlled by you. On the opposite side of the spectrum are serverless 
compute platforms that take Python code and execute it without you ever
touching hardware or even knowing what operating system it runs on. 

In between those extremes are levels that remove the need to worry about
hardware (virtual private servers), up through removing concerns about
web servers (platforms-as-a-service). Where you fall on the spectrum for
your deployment will depend on your own situation. Serverless is simply
the newest and most extreme of these deployment models so it is up to you
as to how much complexity you want to take on with the deployment versus
your control over each aspect of the hardware and software.


### Serverless implementations
Each major cloud vendor has a serverless compute implementation.
These implementations are under significant active developer
and not all of them have Python support.

* [AWS Lambda](/aws-lambda.html) is the current leader among serverless
  compute implementations. It has support for both 
  [Python 2.7](/blog/aws-lambda-python-2-7.html) and 
  [Python 3.6](/blog/aws-lambda-python-3-6.html).
  
* Azure Functions has second-class citizen support for Python. It's
  supposed to be possible but 
  [kind of hacky at the moment](https://github.com/Azure/azure-webjobs-sdk-script/issues/335).
  Polyglot support should be quickly coming to Azure to better
  compete with AWS Lambda.

* IBM Bluemix OpenWhisk is based on the 
  [Apache OpenWhisk](https://github.com/openwhisk/openwhisk)
  open source project.

* [Google Cloud Functions](/google-cloud-functions.html) currently
  only supports JavaScript code execution.

* Webtask.io also only supports JavaScript but there is a cool
  *prototype* project named [webtask-pytask](https://github.com/tehsis/webtask-pytask) 
  to run Python code in the browser via webtask. This demo is definitely not 
  for production code use but awesome to see what the programming community
  can put together using existing code and services.


### Serverless frameworks
Serverless libraries and frameworks aim to provide reusable code that 
handles common or tedious tasks, similar to how 
[web frameworks](/web-frameworks.html) deal with common web development tasks.
Some of these frameworks are built for a single service like AWS Lambda,
while others attempt to make cross-serverless operations more palatable.

Frameworks for building Python-based applications on serverless services 
include:

* [Serverless](https://serverless.com/) ([source code](https://github.com/serverless/serverless)), 
  which is a useful but generically-named library that focuses on deployment 
  and operations for serverless applications.

* [Zappa](https://www.zappa.io/) 
  ([source code](https://github.com/Miserlou/Zappa)) 
  provides code and tools to make it much easier to build on AWS Lambda
  and AWS API Gateway than rolling your own on the bare services.

* [Chalice](https://chalice.readthedocs.io/en/latest/) 
  ([source code](https://github.com/aws/chalice)) is built by the AWS team
  specifically for Python applications.

* [Apex](http://apex.run/) ([source code](https://github.com/apex/apex))


### General serverless resources
Serverless concepts and implementations are still in their early
iterations so there are many ideas and good practices yet to be
discovered. These resources are the first attempts at figuring
out how to structure and operate serverless applications.

* [Serverless software](https://talkpython.fm/episodes/show/118/serverless-software)
  covers a range of topics under serverless and how deployments have
  changed as new options such as [PaaS](/platform-as-a-service.html) 
  have become widespread.

* [Lessons Learned?????????A Year Of Going ???Fully Serverless??? In Production](https://hackernoon.com/lessons-learned-a-year-of-going-fully-serverless-in-production-3d7e0d72213f)
  is a retrospective from a small development team that combines a static 
  site with serverless backend code to easily scale their site without an 
  operations staff. They discuss the good and the bad of working in this
  fashion while generally coming away with a positive experience.

* [Have you shipped anything serious with a ???serverless??? architecture?](https://news.ycombinator.com/item?id=17378749)
  provides some great answers by Hacker News developers who are using
  serverless for large production applications and how they deal with
  the limitations of the platforms.

* [What's this serverless thing, anyway?](https://read.acloud.guru/whats-this-serverless-thing-anyway-b101cb72c7e6)

* [Serverless architectures - let's ditch the servers?](https://codeahoy.com/2016/06/25/serverless-architectures-lets-ditch-the-servers/)

* [The (fixable) problem with serverless](https://www.iopipe.com/2016/06/the-fixable-problem-with-serverless/)

* [Serverless architectures](http://martinfowler.com/articles/serverless.html)
  provides a fantastic overview of the subject with a balanced approach
  that includes the drawbacks seen in current serverless platforms.

* [Why the fuss about serverless?](https://hackernoon.com/why-the-fuss-about-serverless-4370b1596da0)
  is a wide-ranging post about the history of application development and 
  infrastructure. The timeline is a bit hard to follow but otherwise it's
  a unique look at why software deployments are moving to serverless-based
  architectures and the advantages that can provide.

* [Serverless architectures in short](https://specify.io/concepts/serverless-architecture)
  lays out some of the initial thoughts behind what the advantages
  and disadvantages of serverless may be. However, it's early days for
  serverless so these strengths and weaknesses may change as the
  architectures and good practices evolve.

* [Building A Serverless Contact Form For Your Static Site](https://www.smashingmagazine.com/2018/05/building-serverless-contact-form-static-website/)
  uses [AWS Lambda](/aws-lambda.html), some 
  [HTML](/hypertext-markup-language-html.html) and 
  [JavaScript](/javascript.html) to add an input form to a static
  [website created by a static site generator](/static-site-generator.html).

* [Cloud first, serverless second](https://hackernoon.com/cloud-first-serverless-second-1c086f282326)

* [Serverless architectures, five design patterns](https://thenewstack.io/serverless-architecture-five-design-patterns/)
  goes over the four main principles of serverless infrastructure and the
  five major usage patterns the AWS Lambda team is seeing from initial
  serverless deployments.

* [Serverless computing: If there is no server, where does my application run?](https://devup.co/serverless-computing-if-there-is-no-server-where-does-my-application-run-a369c3699730)

* [Serverless Cost Calculator](http://serverlesscalc.com/) estimates
  the amount each serverless platform would charge based on executions,
  average execution time and memory needed per execution. 
  [AWS Lambda](/aws-lambda.html), 
  [Google Cloud Functions](/google-cloud-functions.html),
  Azure Functions and IBM OpenWhisk are all included in the results.


### Serverless vendor lock-in?
There is some concern by organizations and developers about vendor lock-in
on serverless platforms. It is unclear if portability is worse for
serverless than other infrastructure-as-a-service pieces, but still worth
thinking about ahead of time. These resources provide additional 
perspectives on lock-in and using multiple cloud providers.

* [On Serverless, Multi-Cloud, and Vendor Lock In](https://blog.symphonia.io/on-serverless-multi-cloud-and-vendor-lock-in-da930b3993f)
  is an opinion piece that for *most* cases the additional work of
  going multi-cloud is not worth the tradeoffs, therefore at this time
  it's better to go for a single vendor such as AWS or Azure and optimize
  on that platform.

* [Why vendor lock-in with serverless isn???t what you think it is](https://medium.com/@PaulDJohnston/why-vendor-lock-in-with-serverless-isnt-what-you-think-it-is-d6be40fa9ca9)
  is a short piece that also recommends using a single vendor for
  now and stop worrying about hedging your bets because it typically
  makes your infrastructure significantly more complex.

* [The (Fixable) Problem with Serverless](https://www.iopipe.com/2016/06/the-fixable-problem-with-serverless/)
  is a bit of a marketing piece but it introduces 
  [the IOPipe open source projects](https://github.com/iopipe)
  that are designed as an abstraction layer for running on multiple
  serverless cloud platforms.


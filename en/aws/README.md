# Deploy your website on AWS

AWS stands for Amazon Web Services. AWS offers a wide range of cloud services, which include hosting of web 
applications. It was designed to emulate what you would normally have if you were hosting your website on your own 
web servers on your own network using software provisioned services. 

AWS offers new users access to their services for free for 1 year using the [Amazon Free Tier](https://aws.amazon.com/free/) 
when they first sign up. Of course, you need to verify which services are available for you to use for free and for how 
long as some are limited to a certain number of hours per year to avoid being charged as AWS requires you to provide 
a credit card when you sign up.

One way to be sure you don't incur any charges on AWS is to terminate your instances once you are done exploring so that
you don't forget and only be shocked when you receive an AWS bill in you email. So feel free to try out the several ways
to deploy a Django app we have in this tutorial and be sure to shut down all your deployments when you are done. 

Knowledge of AWS or other cloud hosting services is an important skill to have if you plan to pursue a career in tech. 
This tutorial extension is aimed at getting you started with deploying your website to AWS. There are several ways of 
deploying a Django app on AWS which will explore in this part of the tutorial. These include using AWS EC2 and Nginx,
using AWS Lambda to deploy serverless applications or using AWS Elastic Beanstalk. 

We will discuss each of them in turn below.

## AWS Elastic Beanstalk
AWS Elastic Beanstalk is a managed service that can handle our deployment for you. All you need is to push our code and it
will handle the provisioning of all the compute and networking resources for you which is awesome!

## AWS EC2 and Nginx
AWS EC2 server instances provide you with virtual versions of the servers you would normally run in your local data 
centre. You can run a Windows or Linux server using an EC2 instance, and you can provision the instance with CPU, memory, 
storage and network profile to meet the needs of your application, that is, from a simple web server to being one part 
of a cluster of instances for more complicated architectures.

As the primary drive of an EC2 instance comes with a fresh and clean operating system, it is up to you to install the 
software you need to use. This includes the web server software you would want to use to serve your Django website. 
You can Nginx or Apache, both of which are open source web servers, but for the sake of this tutorial, we will use 
Nginx as our web server.

## AWS Lambda
AWS Lambda enables you to deploy your website in a manner in which it is responsive without the need to have the server
run 24/7, an architecture commonly known as being `serveless`. Instead your website will only be spun up in response
to network events such as consumer requests which trigger the execution of your code. Once the operation of your code 
is complete, the server is automatically shut down. 

This kind of deployment would work well for our blog which we do not expect to have lots of traffic to justify running it
24/7.

For the purpose of this tutorial, we will deploy our website using Elastic Beanstalk as it will manage the provisioning of
all the resources we need and works well for first timers with AWS.

However, to be able to use all these resources, one has to create an AWS account and sign up for the free tier.

## Create a free AWS account
If you were working on our main tutorial on a Chromebook, then you have already created an AWS free account for you to 
be able to use AWS Cloud 9 platform. 
You can click `Sign in to an existing AWS account` on [this link](https://portal.aws.amazon.com/billing/signup?refid=em_127222&redirect_url=https%3A%2F%2Faws.amazon.com%2Fregistration-confirmation#/start/email) if you already have an AWS account.
However, if you were not using a ChromeBook and AWS Cloud 9, you need to sign up for a [free AWS account](https://aws.amazon.com/free/). 
From there you can learn more on what is provided by the AWS free tier.


To sign up for AWS, follow the following steps:
1. Click [this link](https://portal.aws.amazon.com/billing/signup?refid=em_127222&redirect_url=https%3A%2F%2Faws.amazon.com%2Fregistration-confirmation#/start/email) and enter your email address and the account name you wish to give your 
account and click `Verify email address` to submit your detail and verify your email address.
2. AWS will send you an email to the email you provided in the previous step with a verification code which you can copy 
and enter in the screen shown below. 
3. The next would be to enter a root password for your account and repeat it as in the screen below. 
Make sure the passwords match and click `Continue (step 1 of 5)` to continue to the next stage.
4. Next, select `Personal Use` and then enter your full name and contact details in the form shown below, country, 
phone number, agree to AWS terms and conditions and then click `Continue (step 2 of 5)` to continue to the next step.
5. The next step would be to provide a credit/debit card with at least a $1 to for AWS to be able verify your identity 
and your billing address in the form below and click `Continue (step 3 of 5)` to continue.
6. This will take you to the next step where you confirm your identity either through a text message (SMS) or voice call 
to your phone. Enter your country, phone number and the security check and click `Continue (step 4 of 5)` to proceed.
7. Enter the code you received and and click `Continue (step 4 of 5)` to proceed.
8. The last step is to select the support plan. We will choose `Basic support - Free` which will cost us nothing for the 
time being and click `Complete signup` to complete the process and create your account. 

Congratulations, you have just created a new AWS account. You can click the `Go to AWS Management Console` to access the
management console.

>>> Please note that sometimes it may take up to 24 hours for your account to be active.

You are now ready to move to the next part of the tutorial.

Let's get started with AWS!

---                          
title: Mentorship Progress
# excerpt_separator: "<!--more-->"
last_modified_at: 2021-08-11T17:12:02-05:00
categories:
  - Blog                     
tags:                  
  - OMP 
  - Mentorship 
  - Polycephaly
---  

Today, I would be talking about my mentorship progress in the Open mainframe project mentorship by the Linux Foundation.
I was accepted into the Polycephaly Project, which from the name “Polycephaly”, means a condition of having more than one head, but in this case, it is called Polycephaly because the project marries two different development life cycle methodologies, distributed and z/OS. This Project is solely developed by my mentor Mr. Jerry Edgington.

Up until I got accepted into the Open Mainframe Mentorship, I had not worked on the mainframe professionally. I have always wanted to learn about it but haven’t had the opportunity.

During the first few weeks of mentorship, I faced the challenge of understanding what the Polycephaly project was all about and how it worked. With my mentor's help through meetings, chats and questions, I got to understand how Polycephaly works and then worked with my mentor by contributing to the Jenkins (CI/CD) pipeline build.

The Polycephaly project is a modern agile approach to software development on the mainframe.
It takes away the burden of interfacing with z/OS off the shoulders of the developer, so the developer has the flexibility and freedom to develop applications on any IDE and deploy to the mainframe.

Now, I would love to share how Polycephaly does the magic.

The Polycephaly java and groovy codes are compiled and are added to the Polycephaly.jar file which is used to run a sample COBOL code.

The entire Software build process is done on a Jenkins slave on z/OS. The Jenkins slave does the bulk of the work by downloading the latest Jenkins slave file to z/OS. The Jenkins slave connects with the git server for the application, pulls and builds the repo and downloads the application source to the repo on z/OS.

Using the build.groovy script, Polycephaly creates an instance of the zOSAppBuild object and with its execute method, the applications build process begins.

Polycephaly has the ability to detect the type of application to be built whether a java, groovy or a COBOL (v4 or v6) source code. It does this by detecting the parameters and properties of the file thereafter, and creates a build list. Using the build list, Polycephaly then creates a build order using the buildOrder function which it uses to determine the order it would use in processing the source files.
 Working on the Polycephaly project has taught me so much about the mainframe. Although this is a fraction of the entire process I promise to always learn more and contribute to the Polycephaly Project.

Thanks.

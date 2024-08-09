# About This Repo and Document
This README serves as a hub for development of a standardized testing training platform called Voeracity, described in more detail below. High level system concepts will be addressed here. Individual services will have their own documentation with more granularity.

# Project Status / Kanban Board
[Project Kanban Board](https://voeracity.atlassian.net/jira/software/projects/V0/boards/1), access available upon request.

# Product Description / Functional Specifications
Voeracity is a standardized test training product. Users can learn exam material, assess learning progress, and take practice tests. In addition to the traditional format of approaching section and subsections in a linear format, an algorithmically driven “Guided Practice” will be available. 

# Wireframes
Lo fi wireframes of the required basic functionality:
![wireframes_alpha](https://github.com/user-attachments/assets/e52e3790-5f6a-4be0-8f4f-35d891a7f8c4)
Note that some views (Sign Up, Log In, Account) have omitted because they are BORING!

# Primary Abstractions
![primary-abstractions](https://github.com/user-attachments/assets/32e7d7d1-e122-40c4-918b-ee4ab34d8e8f)
Pretty straightforward stuff for the time being. These things are always easy at the start eh? Maybe not so much down the road. Anyway, a User can sign up for an Exam, which is made up of Sections, which are made up of Subsections or Modules. The only halfway interesting bit is that Assessments (in this context, an individual question to be answered and graded) can "belong" to both Modules and Practice Exams. 

# Services Architecture
Let's preface this section by saying this architecture is clearly overkill. A monolith on a single server is all that's really needed to get this off the ground and would normally be the advisable way to attack this. However. In this case. I've got some AWS credits to burn and am craving complexity, so we're going to lean in to the loosely-coupled, distributed microservices model, wave our hands a bit, and say something about how well we're positioned to identify bottlenecks and scale efficiently.
![system_design_1_0](https://github.com/user-attachments/assets/4a0971a9-048b-4539-8967-906ee7a88590)
Services and communication channels in the above diagram will turn green as they are brought online. 
Preliminary tech candidates for services are below, lined up with the corresponding piece in the services diagram above. Solutions may change during the development process.
![system_tech](https://github.com/user-attachments/assets/1a120dc0-c988-4947-a72b-5545511afc9f)

# Services

# Deveops and Deploys
All services are containerized with Docker to provide robust scaling options at both ends off the spectrum and ease of dev environment setup.

Details vary by service, but in general commits to main that pass automated testing will be auto-deployed to a text environment. Production deploys are done with a manual green light.

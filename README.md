# About This Repo and Document
This README serves as a hub for development of a standardized testing training platform called Voeracity, described in more detail below. High level system concepts will be addressed here. Individual services will have their own documentation with more granularity.

# Project Status / Kanban Board
[Project Kanban Board](https://voeracity.atlassian.net/jira/software/projects/V0/boards/1), access available upon request.

# Product Description / Functional Specifications
Voeracity is a standardized test training product. Users can learn Exam material, assess learning progress, and take practice tests. In addition to the traditional format of approaching Section and Modules in a linear format, an algorithmically driven “Guided Practice” will be available. 

# Wireframes
![wireframes_alpha](https://github.com/user-attachments/assets/e52e3790-5f6a-4be0-8f4f-35d891a7f8c4)

# Primary Abstractions
![primary-abstractions](https://github.com/user-attachments/assets/32e7d7d1-e122-40c4-918b-ee4ab34d8e8f)

# Services Architecture
![system_design_1_0](https://github.com/user-attachments/assets/4a0971a9-048b-4539-8967-906ee7a88590)
![system_tech](https://github.com/user-attachments/assets/1a120dc0-c988-4947-a72b-5545511afc9f)

# Services

# Deveops and Deploys
All services are containerized with Docker to provide robust scaling options at both ends off the spectrum and ease of dev environment setup.

Details vary by service, but in general commits to main that pass automated testing will be auto-deployed to a text environment. Production deploys are done with a manual green light.

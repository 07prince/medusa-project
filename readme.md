# Medusa E-commerce Platform
### Overview
This project is built on the Medusa open-source headless commerce platform. The project consists of two parts:

1.Backend: Medusa Perl backend for managing e-commerce operations.               
2.Frontend: Medusa Perl storefront for customer-facing interactions.

## Prerequisites
Before you begin, make sure you have the following installed:

1. Node.js (v14 or higher)
2. npm (comes with Node.js)
3. Git
4. PostgreSQL

## Project Setup
 # 1. Clone the Repository
Clone this repository to your local machine:

##### bash

git clone https://github.com/07prince/medusa-project.git

cd medusa-perl


  # 2. Install Dependencies
Install the necessary packages for both the backend and frontend.

### Backend Setup
Navigate to the backend directory:

#### bash
cd medusa-perl
npm install
### Frontend Setup
Navigate to the frontend directory:

#### bash

cd medusa-perl-storefront
npm install

## Running the Project
1. Start the admin
To start the Medusa backend server:

#### bash

cd medusa-perl                                    
npx @medusajs/medusa-cli develop                   

This will start the Medusa backend on http://localhost:70001. You can access the admin panel by going to the /admin endpoint on this URL.

2. Start the Frontend
To start the Medusa storefront (frontend):

#### bash

cd medusa-perl-storefront                              
npm run dev                
The storefront will be accessible at http://localhost:8000.

### Deployment
For deploying this project to production, you can use various hosting options. Below is a general guide on deploying the backend using AWS ECS with Fargate.

Deployment Steps:
#### 1.Dockerize the Backend:

Create a Dockerfile in the medusa-perl directory.
Build and push the Docker image to Docker Hub.
Deploy on AWS ECS:

Create a cluster and task definition in AWS ECS.
Configure the necessary services and network settings.
Set Up a Load Balancer (Optional):

Set up an Application Load Balancer for better traffic management.
Refer to the Medusa documentation for detailed instructions on deployment.

### Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue.


### Contact
For any questions or support, please contact pshahi117@gmail.com.


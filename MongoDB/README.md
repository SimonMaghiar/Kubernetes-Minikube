
In this article, we'll see how kubernetes work in practice and will create a demo application using MongoDB and Express.

![image](https://github.com/SimonMaghiar/Kubernetes-Minikube/assets/43268629/fa057875-95f2-4d28-a8d5-03dd29a9be1b)


**Step 1: Create Secrets**

      We need credentials (username or password) to connect to the database.
      
      So we're going to create a Secret that contains the credentials.
      
      Secret must be created before the deployment. So let's first create a Secret component using the following command:

      1. kubectl apply -f mongo-secret.yml


**Step 2: Create a MongoDB Deployment**

      In K8s we do not directly work with the Pods but there is an abstraction layer over a Pod called Deployment with which we will directly work.

      2. kubectl apply -f mongo-deployment.yml

**Step 3: Create an Internal service for MongoDB**

      First, we created a MongoDB pod and to talk to that pod we will need an internal service, which means no external request to that pod is allowed. Only components inside the same cluster can talk to it.

      3. kubectl apply -f mongo-service.yml

**Step 4: Config Map for Express App**

      4. kubectl apply -f mongo-configmap.yml

**Step 5: Create an Express deployment**

      5. kubectl apply -f mongo-express.yml

**Step 6: Create an External Service for Express App**

      We need an external service so that it can be accessed through a browser.

      6. kubectl apply -f express-service.yaml

![image](https://github.com/SimonMaghiar/Kubernetes-Minikube/assets/43268629/1d14e2bc-4959-43d4-ba9c-15ed83859f80)
![image](https://github.com/SimonMaghiar/Kubernetes-Minikube/assets/43268629/284baf3a-9a65-4c54-b536-9e4ce73f8a73)
![image](https://github.com/SimonMaghiar/Kubernetes-Minikube/assets/43268629/f763effe-5c62-4bc1-b004-c670c9e781db)




      


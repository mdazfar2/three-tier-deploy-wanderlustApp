# Three Tier Wanderlust App.........

![3-tier-wanderlust](https://github.com/mdazfar2/three-tier-deploy-wanderlustApp/assets/100375390/825e7505-ae46-46da-8835-7bba890ed1f5)

## Overview- 

Welcome to Wanderlust! This three-tier travel app, powered by React.js, Node.js, and MongoDB, is your gateway to discovering exciting destinations, seamlessly deployed on AWS and Docker! 🌍✈️

# Step by Step guide for making this project-

  1. Fork this repo or clone-
     ```bash
     git clone https://github.com/mdazfar2/three-tier-deploy-wanderlustApp.git
     ```

  2. Install docker and docker-compose

  3. Go to the `backend` directory
     ```bash
     cd three-tier-deploy-wanderlustApp/backend
     ```

  4. Then go to the `.env.sample` file and edit, paste your public ec2-ip & then save
     ```bash
     vim .env.sample
     ```
     ![.env.sample file](https://github.com/mdazfar2/three-tier-deploy-wanderlustApp/assets/100375390/4e322317-9631-4eee-9b0f-55fdddfe0065)

  5. And then build image for `backend`
     ```bash
     docker build -t backend .
     ```

  6. Now move back to the `frontend` directory
     ```bash
     cd ../frontend
     ```
  7. Then again go to the `.env.sample` file and edit, and paste your public ec2 id & then save
     ```bash
     vim .env.sample
     ```
     ![image](https://github.com/mdazfar2/three-tier-deploy-wanderlustApp/assets/100375390/ae48cd24-e220-403f-a79b-cc86de7f0c0d)

  8. Then build the image for `frontend`
     ```bash
     docker build -t frontend .
     ```

  9. Now, navigate to the main directory of our project, which is `three-tier-deploy-wanderlustApp`.
      ```bash
      cd ..
      ```

  10. Now run the docker-compose-
      ```bash
      docker-compose up -d --build
      ```
  11. Now go the Inside the mongoDB container for Import sample data
      ```bash
      docker exec -it <ur-containerID-of-mongo> mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray
  11. Now use your <EC2-public-Ip> with port:5173
      ```
      EC2-public-Ip:5173
      ```

      ***After this it will be running fine and well, if you are facing any issues, please don't hesitate to ask me. You can connect with me on-***

- [LinkedIN](https://linkedin.com/in/md-azfar-alam)
- [Discord](https://discordapp.com/users/877531143610708028)
- [Mail Me](mailto:azfaralam.ops@gmail.com)

  ---
  
### Will also deploy it using kubernetes, stay tuned! Thanks :)

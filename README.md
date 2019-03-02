# symfony-demo-app

## Instructions:

1. You have to create a **Dockerfile**, with:
    * Install git
    * Install symfony

2. You have to create a **docker-compose.yml** file, with the symfony service declared as follows:
    * Image stucom/php
    * Volumes defined
    * Ports defined

3. You have to compile the **stucom/php** image with the following command:

    `docker-compose build`
    
4. Once you've completed the previous steps, you'll be able to create your demo application with the following command:

    ``docker run --rm -v `pwd`/src:/var/www -w /var/www stucom/php symfony new --demo symfony-demo-app``

5. Run the following commands to start your new demo application: 

    `docker-compose up -d` 
    
    `docker-compose exec symfony chown -R www-data:www-data .` 

Now you can go to **http://localhost** in your browser, you have to see the symfony demo page.


## Bonus:
Modify the Dockerfile and docker-compose.yml files to simulate a deploy to production environment. 

Tip: the source code should not be a volume, it has to be part of the Docker image.

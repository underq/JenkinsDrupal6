DrupalSample 
============

I try to do CI with Drupal & Jenkins


Installation
============

Step 1: Installation
--------------------

__Installation de Jenkins__
>* wget -q -O http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
>* echo "\nhttp://pkg.jenkins-ci.org/debian binary/" | tee -a /etc/apt/sources.list 
>* sudo apt-get install jenkins

__Installation de GIT__
>* sudo apt-get install git-core

__Installation de PHP & PEAR__
>* sudo apt-get install php5
>* sudo apt-get install php-pear
>* sudo pear upgrade-all

__Installation de drush__
>* sudo pear channel-discover pear.drush.org
>* sudo pear install drush/drush
>* sudo pear upgrade --force Console_Getopt
>* sudo drush --version

__Recuperation du Jenkins-cli.jar pour l'utilisation en ligne de commande__
>* wget http://localhost:8080/jnlpJars/jenkins-cli.jar

__Installation des plugins Jenkins__
>* sudo java -jar jenkins-cli.jar -s http://localhost:8080 install-plugin checkstyle
>* sudo java -jar jenkins-cli.jar -s http://localhost:8080 install-plugin ci-game
>* sudo java -jar jenkins-cli.jar -s http://localhost:8080 install-plugin dry
>* sudo java -jar jenkins-cli.jar -s http://localhost:8080 install-plugin pmd
>* sudo java -jar jenkins-cli.jar -s http://localhost:8080 install-plugin git
>* sudo java -jar jenkins-cli.jar -s http://localhost:8080 safe-restart



Step 2: Configuration 
---------------------

__GIT__
>* Générer une cle ssh pour l'utilisateur jenkins
>* ssh-keygen -t rsa -C "your_email@youremail.com"
>* L'ajouter au _authorized_keys_ du server GIT
>* ssh UserGIT@IpServerGIT "echo $(cat ~/.ssh/id_rsa.pub) >> .ssh/authorized_keys"

Step 3 :
--------
Install de tous les plugin d'analyse de code PHP
 - PHP_Documentor (Pour drupal ajouter les extentions module et intall au phpDocumentor.ini)
 - PHP_CodeSniffer (Ajouter les coding standard de drupal http://drupal.org/project/drupalcs) 



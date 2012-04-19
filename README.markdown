DrupalSample 
============

I try to do CI with Drupal & Jenkins


Installation
============

__Installation de Jenkins__
>* wget -q -O http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
>* echo "\nhttp://pkg.jenkins-ci.org/debian binary/" | tee -a /etc/apt/sources.list 
>* sudo apt-get install jenkins

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
>* java -jar jenkins-cli.jar -s http://localhost:8080 install-plugin checkstyle

Step 1 :
--------
Install Jenkins on your OS.
http://aaronbonner.tumblr.com/post/8339092868/installing-jenkins-on-ubuntu

Step 2 :
--------
Install PEAR & Mise à jour de la derniere version (pear upgrade-all)

Step 3 :
--------
Install de tous les plugin d'analyse de code PHP
 - PHP_Documentor (Pour drupal ajouter les extentions module et intall au phpDocumentor.ini)
 - PHP_CodeSniffer (Ajouter les coding standard de drupal http://drupal.org/project/drupalcs) 



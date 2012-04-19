DrupalSample 
============

I try to do CI with Drupal & Jenkins


Installation
============

* wget -q -O http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
* sudo apt-get install jenkins
* sudo apt-get install php5
* sudo apt-get install php-pear

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



pipeline {
	agent{
	label 'Mens-lable'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/grras/slave-dir/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/grras5.war /home/grras/slave-dir/apache-tomcat-9.0.82/webapps'
			}}	
}}

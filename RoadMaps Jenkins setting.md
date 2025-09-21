Install jenkins

check status of jnekins (open port 8080)

cat /password/ admin

for plugin :

 - clique on : Manage Jenkins > Plugins > Available Plugins

choose : 

1 Eclipse Temurin Installer (Install without restart)

2 SonarQube Scanner (Install without restart)

3 NodeJs Plugin (Install Without restart)

 - Tools section
 
  jdk and nodejs ( choose name that we gonna use in jenkins script CICD
  
  tools {
    jdk 'name'
	nodejs 'name'
  }


** For SonarQube we need to connect sonnar to jenkins before finish the sitting in jenkins


<> On SonarQube > middel page clique on Administration > Security > Users > Administator right generation token , put a name>>< , and copy the token 

comeback to Jenkins > clique on creadention option > system > Global credential > new credential > choose secret text ...

<> manage jenkins > system > SonarQube > name : sonar_server
                                         url : ipadresse:9000
										 serveur authentificatin : choose token
										 
<> add SonarQube Scanner:
manae jenkins > tools > search for SonarQubeScanner > put name (script)

Configuration is ready !!!!

<> pick up a Pepline

new items > name <netflix(exammple) > clique on pipline	> add the pipline script


** add more plugin docker and owasp dependency check 
tools > owasp dependency> > name (script) > 


** add credential for docker to push the image in repo							  
										
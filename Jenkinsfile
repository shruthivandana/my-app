node{
   stag":il.uk,iyjmuthnyfrgdthfyguihjoip[o]p[\'Docker Image Push'){
   withCredentials([string(credentialsId: 'dockerPass', variable: 'dockerPassword')]) {
   sh "docker login -u saidamo -p ${dockerPassword}"
    }
   sh 'docker push saidamo/myweb:0.0.2'
   }
   
   stage('Remove Previous Container'){
	try{
		sh 'docker rm -f tomcattest'
	}catch(error){
		//  do nothing if there is an exception
	}
   stage('Docker deployment'){
   sh 'docker run -d -p 8090:8080 --name tomcattest saidamo/myweb:0.0.2' 
   }
}
}][
	]

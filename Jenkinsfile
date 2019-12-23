node('centos6'){
	stage('构建'){
		//把代码从git上clone下来
		checkout scm	
	}
	stage('部署'){
	
		sh 'cd restapi-teach && sh run.sh'
	}
	stage('测试'){
		//指定脚本在本地执行，不在节点上运行
		node(){
			checkout scm
			bat 'robot -P . course'
		
		}
	}
	stage('交付'){
	//delivery
	}

}
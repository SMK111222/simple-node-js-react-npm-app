pipeline {
    agent {
        docker {
            // 更新为 Node 18 (LTS版本)，Node 6 太老了不支持现代 React
            image 'node:18-alpine' 
            // 映射端口，方便测试
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                // 打印 Node 版本，确认环境正确
                sh 'node -v'
                // 安装依赖
                sh 'npm install' 
            }
        }
        // (可选) 你可以在这里添加 Test 或 Deliver 阶段
    }
}
pipeline {
    agent any

    stages {
        stage('1. Checkout Code') {
            steps {
                // Git SCM 설정에 따라 Jenkins가 자동으로 코드를 가져옵니다.
                echo 'Git 저장소에서 소스 코드 Checkout 완료.'
            }
        }

        stage('2. Verify Files') {
            steps {
                echo '=== 파일 존재 및 내용 확인 ==='
                
                // [방법 1] 'version.txt' 파일의 내용을 직접 읽어와 출력
                sh 'echo "Version read from file: $(cat version.txt)"'
                
                // [방법 2] 'app.py' 파일이 실제로 존재하는지 목록 확인
                sh 'ls -l app.py'
            }
        }
        
        stage('3. Show Environment') {
            steps {
                echo '=== 현재 Git 정보 출력 ==='
                // Jenkins가 가져온 현재 Git 커밋 ID 출력
                sh 'echo "Current Git Commit: ${GIT_COMMIT}"' 
            }
        }
    }
}

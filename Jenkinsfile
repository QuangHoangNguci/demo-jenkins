CODE_CHANGES = getGitChanges()
pipeline {
  agent any

  parameters {
    choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'Choose the version to deploy')
    booleanParam(name: 'executeTests', defaultValue: true, description: 'Set to true to execute tests')
  }

  stages {
    stage("build") {
      steps {
        echo 'Building the application...'
        // Thêm các bước xây dựng ứng dụng (build steps) ở đây nếu cần thiết
      }
    }

    stage("test") {
      when {
        expression {
          params.executeTests
        }
      }
      steps {
        echo 'Testing the application...'
        // Thêm các bước kiểm thử ở đây nếu cần thiết
      }
    }

    stage("deploy") {
      steps {
        echo 'Deploying the application...'
        echo "Deploying version ${params.VERSION}"
        // Thêm các bước triển khai ứng dụng ở đây nếu cần thiết
      }
    }
  }
}

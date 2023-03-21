pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        sh 'python3 -m venv ~/venv'
        sh 'python3 -m pip install --upgrade pip wheel'
        sh 'pip install -r requirements.txt'
      }
    }

    stage('Run tests') {
      steps {
        sh 'nosetests -vv --with-spec --spec-color --with-coverage --cover-package=service'
      }
    }

  }
}
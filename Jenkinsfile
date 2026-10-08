
pipeline {
    agent any

    parameters {
        // Defines the first integer parameter
        string(
            name: 'NUM_A', 
            defaultValue: '0', 
            description: 'First integer number'
        )
        
        // Defines the second integer parameter
        string(
            name: 'NUM_B', 
            defaultValue: '0', 
            description: 'Second integer number'
        )
    }

    stages {
        stage('Validate & Process') {
            steps {
                script {
                    // Jenkins parameters are passed as Strings, so we convert them to Integer
                    def num1 = params.NUM_A.toInteger()
                    def num2 = params.NUM_B.toInteger()
                    
                    echo "Successfully received numbers: ${num1} and ${num2}"
                    
                    // Example operation: Adding the numbers together
                    def result = num1 * num2
                    echo "The multiplication of ${num1} * ${num2} is: ${result}"
                }
            }
        }
    }
}

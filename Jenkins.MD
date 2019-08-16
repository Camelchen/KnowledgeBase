#### Installation
* set up SSH for Jenkins

#### Jenkinsfile
* change runtime the location
    ```jenkins
    dir(%PATH%){
        stage() { ... }
        stage() { ... }
    }
* try...catch...finally
    ```jenkins
    try(){
        stage() { ... }
        stage() { ... }
    }
    catch(error){
        ....
        throw e
    }
    finally{
        ....
    }

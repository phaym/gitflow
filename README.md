# gitflow

- merge pr
  - create image / push to gcp 
    - tag main-{sha}
  - update tag version
  - deploy to qa
- deploy to qa
  - GA    
  ```
    func deploy(sha=null) {
        deploySha = sha ?? getCommit('HEAD')
        let tags = getTags(deploySha)
        trigger.deploy(tag, triggerUri)
    }
    ```
 }
- deploy to prod

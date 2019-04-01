# GoCD-pipeline-sample-json
GoCD sample pipelines using json config plugin. 
There is a docker-compose file which creates gocd-server and gocd-agent along with opening respective ports.

## Prerequisites::
 - Make sure docker and docker-compose is installed.

 
## Server Confiuration::
 - Navigate to gocd server using your browser.
```xml
http://<localhost>:8153
http://<your-machine-ip-address>:8153
```
 - Make sure the agent is enabled. 
 - Add this to your cruise-config.xml configuration:
```xml

<config-repos>
   <config-repo pluginId="json.config.plugin" id="test-repo1">
     <git url="https://github.com/NikAraga/gocd-pipeline-sample-json.git" />
   </config-repo>
</config-repos>
```
 - This will automatically create a new pipeline within the gocd server.

### References::
 These resources will help to navigate through more details about the GoCD tool and usage of GoCD json config plugin.
  - [GoCD Tool](https://www.gocd.org/)
  - [GoCD Json Config Plugin](https://github.com/tomzo/gocd-json-config-plugin)
  - [GoCD Json Config Plugin Example](https://github.com/tomzo/gocd-json-config-example)
  - [Pipelines as code](https://docs.gocd.org/current/advanced_usage/pipelines_as_code.html)
  - [A Sample GoCD Pipeline](https://pnguyen.io/posts/a-sample-gocd-pipeline)

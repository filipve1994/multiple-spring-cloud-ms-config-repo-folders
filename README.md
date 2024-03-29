# multiple-spring-cloud-ms-config-repo-folders
public repo with general settings for all kind of microservices for spring cloud config server for general use of project specific in subfolders

## subfolder structure

- common-config
  - => this folder contains config files for whatever kind of project with general settings to reuse
  - => for example, eureka-service-discovery, gateway-general-settings, DB settings, docker settings etc.
- project-config
  -  => this folder will contain config files for sample-projects, other kind of projects etc.
  -  => for example department-service, user-service, auth-service, mail-service, etc.
  -  => group per project, or per application, or both etc.
  -  => need to think for a good structure

## convert properties to yaml online

- https://env.simplestep.ca/
- https://www.baeldung.com/spring-boot-convert-application-properties-to-application-yml

## Links

- https://docs.spring.io/spring-cloud-config/docs/current/reference/html/#_spring_cloud_config_client

- https://www.google.com/search?q=spring+cloud+config+server+combine+multiple+config+repos
- https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html
- https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html#composite-environment-repositories
- https://stackoverflow.com/questions/61443588/adding-multiple-repositories-to-spring-cloud-config-server
- https://stackoverflow.com/questions/51737545/spring-cloud-config-multiple-composite-repositories
- https://stackoverflow.com/questions/51737545/spring-cloud-config-multiple-composite-repositories

- https://medium.com/@pravinbabu4u/spring-cloud-config-best-practices-19c51a71687d
- https://github.com/spring-cloud/spring-cloud-config/issues/286
- https://docs.spring.io/spring-cloud-config/reference/server/environment-repository/composite-repositories.html
- https://medium.com/jamalsoliva/spring-cloud-config-server-with-multiples-repositories-d8aeaa5fc41c
- https://stackoverflow.com/questions/67573510/spring-cloud-config-serving-multiple-applications-which-has-multiple-configura
- 


- https://docs.spring.io/spring-cloud-config/reference/server/environment-repository/overriding-properties-using-placeholders.html
- https://docs.spring.io/spring-cloud-config/reference/server/environment-repository/overriding-properties-using-profiles.html

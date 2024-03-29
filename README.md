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

## information

#### Querying the Configuration
Now we’re able to start our server. The Git-backed configuration API provided by our server can be queried using the following paths:

```
/{application}/{profile}[/{label}]
/{application}-{profile}.yml
/{label}/{application}-{profile}.yml
/{application}-{profile}.properties
/{label}/{application}-{profile}.properties
```

The {label} placeholder refers to a Git branch, {application} to the client’s application name, and the {profile} to the client’s current active application profile.

So we can retrieve the configuration for our planned config client running under the development profile in branch master via:

$> curl http://root:s3cr3t@localhost:8888/config-client/development/master

https://docs.spring.io/spring-cloud-config/docs/current/reference/html/#_locating_remote_configuration_resources

##### Locating Remote Configuration Resources

The Config Service serves property sources from /{application}/{profile}/{label}, where the default bindings in the client app are as follows:

"application" = ${spring.application.name}

"profile" = ${spring.profiles.active} (actually Environment.getActiveProfiles())

"label" = "master"

When setting the property ${spring.application.name} do not prefix your app name with the reserved word application- to prevent issues resolving the correct property source.
You can override all of them by setting spring.cloud.config.* (where * is name, profile or label). The label is useful for rolling back to previous versions of configuration. With the default Config Server implementation, it can be a git label, branch name, or commit ID. Label can also be provided as a comma-separated list. In that case, the items in the list are tried one by one until one succeeds. This behavior can be useful when working on a feature branch. For instance, you might want to align the config label with your branch but make it optional (in that case, use spring.cloud.config.label=myfeature,develop).

## Links

- https://www.baeldung.com/spring-cloud-configuration

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

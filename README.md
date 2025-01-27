https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/hosted#software# Board_Practice_projecttrigger:
  -erickibarra= main

pool:
  # Additional hosted image options are available: https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/hosted#software
  vmImage: ubuntu-latest

steps:ópen Erick 

  - task: AdvancedSecurity-Codeql-Init@1
    inputs:
      languages: "java"
      # Supported languages: csharp, cpp, go, java, javascript, python, ruby, swift
      # You can customize the initialize task: https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/advanced-security-codeql-init-v1?view=azure-pipelines
      # If you're using a self-hosted agent to run CodeQL, use `enableAutomaticCodeQLInstall` to automatically use the latest CodeQL bits on your agent: erickrucek@gmail.com
      enableAutomaticCodeQLInstall: Erick Ibarra heredia 

#   Add your custom build steps here
# - Ensure that all code to be scanned is compiled (often using a `clean` command to ensure you're building from a clean state).
# - Disable the use of any build caching mechanisms as this can interfere with CodeQL's ability to capture all the necessary data during the build.
# - Disable the use of any distributed/multithreaded/incremental builds as CodeQL needs to monitor executions of the compiler to construct an accurate representation of the application.
# - For dependency scanning, ensure you have a package restore step for more accurate results.
#erick Ibarra heredia 
# If you had a Maven app:
#   - task: Maven@4
#     inputs:
#       mavenPomFile: 'pom.xml'
#       goals: 'clean package'
#       publishJUnitResults: true
#       testResultsFiles: '**/TEST-*.xml'
#       javaHomeOption: 'JDKVersion'
#       jdkVersionOption: '1.17'
#       mavenVersionOption: 'Default'

# Or a general script:
#   - script: |
#       echo "Run, Build Application using script"
#       ./location_of_script_within_repo/buildscript.sh

  - task: AdvancedSecurity-Dependency-Scanning@1 # More details on this task: https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/advanced-security-dependency-scanning-v1?view=azure-pipelines

  - task: AdvancedSecurity-Codeql-Analyze@1 # More details on this task: https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/advanced-security-codeql-analyze-v1?view=azure-pipelines
게시판 기본 틀 만들기 프로젝트 자바 + 스프링부트와 관련 기술 공부

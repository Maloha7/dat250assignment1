# Dat250assignment1
Marius Hatland 29.08.2023

## Link to docker image on docker hub
https://hub.docker.com/repository/docker/maloha7/dat250/tags?page=1&ordering=last_updated

## Technical problems during installation

The only technical problem I encountered during installation was when trying to install gradle. At first, I tried installing it via the apt package manager in ubuntu. After installing it and trying to run gradle init i encountered the following error message: 
> Could not create service of type ScriptPluginFactory using BuildScopeServices.createScriptPluginFactory().
> Could not create service of type PluginResolutionStrategyInternal using BuildScopeServices.createPluginResolutionStrategy().

I tried searching for a solution but none of the suggested actions I found online helped resolve the issue. My solution was then to uninstall gradle and try installing it via sdk man. This fixed the issue and I was able to continue with the assignment.

## Validation of software environment
To validate that the software environment is working correctly I built and ran the project locally, verifying that there were no build errors and that the application was working correctly in a web browser.
I then validated that the project would work on other computers by creating a docker image, publishing it to docker hub and then pulling the image and testing it locally.

## Technical problems
I encountered a few technical problems while working on the project. 
One issue that happened was that my IDE(intelliJ) were unable to parse the build.gradle.kts file.
> Cannot access script base class 'org.gradle.kotlin.dsl.KotlinBuildScript'. Check your module classpath for missing or conflicting dependencies.

Another issue was a build error which said:
> Task 'wrapper' not found in project ':app'.
>* Try:
> Run gradle tasks to get a list of available tasks.
> For more on name expansion, please refer to https://docs.gradle.org/8.3/userguide/command_line_interface.html#sec:name_abbreviation in the Gradle documentation.
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.
> Get more help at https://help.gradle.org.
BUILD FAILED in 7s

I'm not sure if these problems were related or not, but I was able to fix both of them by reloading all gradle project in the IDE and the rebuliding the project.

## Pending issues

I have no pending issues in my software development environment.
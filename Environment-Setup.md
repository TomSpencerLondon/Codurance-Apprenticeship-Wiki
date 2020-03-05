# Java Project Creation Scripts
During the apprenticeship training programme, you will frequently be creating new projects, importing them into your IDE and initialising empty Git repositories. For Java devs working on Unix-based operating systems, there are a pair of scripts to automate this process for you. There is one script for Maven projects and one for Gradle projects.

After installing either script (see below), you can use it to create a project like this:

```bash
$ project <project name>
```

It will create the project directory in your current working directory, create the necessary structure inside, add a build script and an appropriate .gitignore file, initialise an empty git repository, and commit the build script and .gitignore file. The project will now be ready to import into your IDE (IntelliJ is assumed).

## Maven Projects
Copy & paste the following command into your terminal:

```bash
sudo curl --progress-bar https://raw.githubusercontent.com/richardjwild/miscellaneous/master/maven-project.sh > /usr/local/bin/project && sudo chmod 755 /usr/local/bin/project
```

## Gradle Projects
Copy & paste the following command into your terminal:

```bash
sudo curl --progress-bar https://raw.githubusercontent.com/richardjwild/miscellaneous/master/gradle-project.sh > /usr/local/bin/project && sudo chmod 755 /usr/local/bin/project
```

## .NET Core on Mac/Linux

You can find a crude bash script that speeds up the creation of a new .Net Core console application at https://raw.githubusercontent.com/christopher-bimson/Scripts/master/bash/dotnetcore-console-project.sh
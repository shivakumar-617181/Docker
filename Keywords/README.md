Docker File:-

A Dockerfile is a plain Text Document that Contains a Set of Instructions Used to Build a Docker Image.Each Instruction in a Dockerfile Represents A Step In The Image Creation Process, Those Commands Wil be Executed From Top to Bottom. We Have to Write The Instructions in DSL It Containes Set of KeyWords. Based On The Key Words the Instructions in the Docker file Will Be Executed.

Instructions:-
FROM
MAINTAINER
WORKDIR
ENV
USER
LABEL
COPY
ADD
RUN
CMD
ENTRYPOINT
EXPOSE

**Explanation:-**

**FROM:-**
 FROM Keyword Indiates that Base Image Which We are Going to Use for Our Image.
 
**MAINTAINER:-**
 It will be Ued as Comments to Describe author/owner, Who is Maintaining the Docker File.
 
**WORKDIR:-**
 This Keyword Used to Set the a Working Directory the Current Working Directory and Used on Which Directory Our Instruction are Going to Execute.
 
**ENV:-**
 This Instruction is Used to Setup the Environment Varaibles For Our Container/Image.
 
**USER:-**
 This key word is used to set the user for the container. If you didnot mentioned the user name by default the commands will be executed as root user.
 
**LABEL:-**
 It is Used to label the image for identifucation purpose.
 LABEL <key> <value>
 
**COPY:-**
 This Keyword Is Used to Copy Files From Host Server to Container. It is Simple Straight forward Copying the files.
 Syntax:- COPY <Source> <dest>
 
**ADD:-**
 It Can also Used for Copying files from Host Server to Container. It has several Advantages when compared to COPY keyword. Like It will automatically extract the .tar.gz files & Adding the files from Remote URL files to our Image.
  Syntax:- ADD <Source> <dest>
  
**RUN:-**
 RUN Command will be executed while creating the Image.

**CMD**
 CMD Commands Will be Passed as Arguments for The ENTRYPOINT. CMD Commanns Are Easily Overridden by Docker Run Passing Arguments and ENTRYPOINT arguments. CMD arguments are used to pass Default arguments for container, you can override those later.  CMD Instruction Will Be Executed While Creating the Container. 
 Syntax:- CMD [ "java", "-jar", "springapplication.jar"]

**ENTRYPOINT:-**
 ENTRYPOINT is Mostly used for the Starting the Container Commands i.e., Prdefined Commands for Starting Of The Container. Any Arguments Provided With docker run are Appended to the ENTRYPOINT Command as Arguments. CMD arguments will be over ridden. 
  Syntax:- ENTRYPOINT [ "java", "-jar", "springapplication.jar"]

  ** If you are Using <docker run img /etc/passwd> In This </etc/passwd> is command. and if you have used ENTRYPOINT as ["/bin/cat"]. Then Result of execution for the container is /bin/cat /etc/passwd.

**Docker has a default entrypoint which is /bin/sh -c but does not have a default command/argument**

 
**EXPOSE;-**
 EXPOSE key word is used to specify the port on which port container will runs.
  NOTE:- It is Just for documentation purpose. Not for opening the for port that container.




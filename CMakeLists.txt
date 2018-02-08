cmake_minimum_required(VERSION 3.5)

find_package(Java REQUIRED)
include(UseJava)

project(Eole)

set(SRCS
	src/Window.java 
	src/Regate.java 
	src/Participant.java 
	src/ModifRegate.java
	src/Main.java
	src/LancementRegate.java
	src/DTimer.java
	src/Classement.java
	src/ButtonRenderer.java
	src/ButtonEditor.java
	src/Bdd.java
	src/AjoutRegate.java
	src/AjoutParticipant.java
	src/Accueil.java
    )

set(JAR
	lib/mysql-connector-java-5.0.5-bin.jar
    	lib/jcalendar-1.4.jar
    )

add_jar(eole 
	SOURCE ${SRCS}
	INCLUDE_JARS ${JAR}
	OUTPUT_DIR ${PROJECT_BINARY_DIR}/build
       )


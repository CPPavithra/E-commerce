1.	Create a new folder in C: (I used C:\MyWorkspace)
2.	Open the Eclipse and choose this folder
3.	New-> Dynamic Web Project ->Sports-Store
4.	Add new folder src/main/resources, src\main\webapp (This is the area where your JSP/CSS/HTML pages resides)
5.	Click “Generate web.xml deployment description”
6.	Right click->configure-> Convert to Maven Project
7.	Check Properties->Deployment Assembly->Add Maven Dependency if not there
8.	Properties->Project Facets -> Click “Apache TomCat” in runtimes
9.	If runtimes is blank, then we need to add it
a.	Apache Tomcat v10.1
b.	Installation directory - D:\Softwares\apache-tomcat-10.1.24
10.	Add Server Runtime [Apache Tomcatv10.1] to Classpath
11.	Add the dependencies in pom.xml file
12.	Create the packages one by one. Instead of com.shashi.serv I used com.nka.serv (nka stands for Nikhil-Kshitij-Aditya)
13.	Create the class in each package
14.	Copy the file content from old project to your project
15.	Replace “Shashi” with “nka”

Add the below in pom.xl (the exact location of index.jsp) – under <artifactId>maven-war-plugin</artifactId>
        <version>3.2.3</version>


<configuration>	
<warSourceDirectory>src/main/webapp/WEB-INF</warSourceDirectory>
</configuration>


Errors – 
The default superclass, "jakarta.servlet.http.HttpServlet", according to the project's Dynamic Web Module facet version (5.0), was not found on the Java Build Path
Solution – Download the latest API and copy to pom.xml

File Structure
1.	application.properties (under src/main/java)
a.	It has all the path properties of the project like db connection string and mail Ids
2.	Expense UI Page

	
                AddExpenseSrv.java (com.nka.srv) // IT COLLECTS ALL UI DATA AND PASS TO NEXT LEVEL

	
                ExpenseServiceImpl.java (com.nka.service.impl) 	//GETS THE DATA AND ACTUALLY WRITES TO DB


1.	ExpenseService.java (com.nka.service)	//JUST DECLARES ALL THE FUCNTIONS USED IN impl.java
2.	ExpenseBean.java (com.nka.beans)	//Actual class with variables and get set member functions


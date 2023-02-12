This project is regarding CRUD Spring MVC architecture using hibernate, jsp used with jstl library for frontend
give db credential in WEB-INF folder servlet-context.xml

firstly create table in db
 create table person ( id int primary key auto_increment,name varchar(35),country varchar(35));
  insert into person (id,name,country) values (1,'sagar','India'),(2,'satya','rusia');
  
  run on server (apache tomacat configure before run)

  
  
  
---------------------------------------------CONSOLE OUTPUT-------------------------------------------------------  
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Server version name:   Apache Tomcat/9.0.65
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Server built:          Jul 14 2022 12:28:53 UTC
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Server version number: 9.0.65.0
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: OS Name:               Windows 11
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: OS Version:            10.0
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Architecture:          amd64
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Java Home:             C:\Users\HP\.p2\pool\plugins\org.eclipse.justj.openjdk.hotspot.jre.full.win32.x86_64_19.0.1.v20221102-1007\jre
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: JVM Version:           19.0.1+10
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: JVM Vendor:            Eclipse Adoptium
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: CATALINA_BASE:         D:\Applications\Eclipse IDE\Eclipse_1\.metadata\.plugins\org.eclipse.wst.server.core\tmp0
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: CATALINA_HOME:         D:\projects\JarFiles\Servlet-tomcat jar file\apache-tomcat-9.0.65-windows-x64\apache-tomcat-9.0.65
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: -Dcatalina.base=D:\Applications\Eclipse IDE\Eclipse_1\.metadata\.plugins\org.eclipse.wst.server.core\tmp0
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: -Dcatalina.home=D:\projects\JarFiles\Servlet-tomcat jar file\apache-tomcat-9.0.65-windows-x64\apache-tomcat-9.0.65
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: -Dwtp.deploy=D:\Applications\Eclipse IDE\Eclipse_1\.metadata\.plugins\org.eclipse.wst.server.core\tmp0\wtpwebapps
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: --add-opens=java.base/java.lang=ALL-UNNAMED
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: --add-opens=java.base/java.io=ALL-UNNAMED
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: --add-opens=java.base/java.util=ALL-UNNAMED
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: --add-opens=java.base/java.util.concurrent=ALL-UNNAMED
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: --add-opens=java.rmi/sun.rmi.transport=ALL-UNNAMED
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: -Dfile.encoding=UTF-8
Feb 12, 2023 1:50:11 PM org.apache.catalina.startup.VersionLoggerListener log
INFO: Command line argument: -XX:+ShowCodeDetailsInExceptionMessages
Feb 12, 2023 1:50:11 PM org.apache.catalina.core.AprLifecycleListener lifecycleEvent
INFO: Loaded Apache Tomcat Native library [1.2.35] using APR version [1.7.0].
Feb 12, 2023 1:50:11 PM org.apache.catalina.core.AprLifecycleListener lifecycleEvent
INFO: APR capabilities: IPv6 [true], sendfile [true], accept filters [false], random [true], UDS [true].
Feb 12, 2023 1:50:11 PM org.apache.catalina.core.AprLifecycleListener lifecycleEvent
INFO: APR/OpenSSL configuration: useAprConnector [false], useOpenSSL [true]
Feb 12, 2023 1:50:11 PM org.apache.catalina.core.AprLifecycleListener initializeSSL
INFO: OpenSSL successfully initialized [OpenSSL 1.1.1q  5 Jul 2022]
Feb 12, 2023 1:50:12 PM org.apache.coyote.AbstractProtocol init
INFO: Initializing ProtocolHandler ["http-nio-8080"]
Feb 12, 2023 1:50:12 PM org.apache.catalina.startup.Catalina load
INFO: Server initialization in [1341] milliseconds
Feb 12, 2023 1:50:12 PM org.apache.catalina.core.StandardService startInternal
INFO: Starting service [Catalina]
Feb 12, 2023 1:50:12 PM org.apache.catalina.core.StandardEngine startInternal
INFO: Starting Servlet engine: [Apache Tomcat/9.0.65]
Feb 12, 2023 1:50:16 PM org.apache.jasper.servlet.TldScanner scanJars
INFO: At least one JAR was scanned for TLDs yet contained no TLDs. Enable debug logging for this logger for a complete list of JARs that were scanned but no TLDs were found in them. Skipping unneeded JARs during scanning can improve startup time and JSP compilation time.
Feb 12, 2023 1:50:16 PM org.apache.catalina.core.ApplicationContext log
INFO: No Spring WebApplicationInitializer types detected on classpath
Feb 12, 2023 1:50:17 PM org.apache.catalina.core.ApplicationContext log
INFO: Initializing Spring root WebApplicationContext
INFO : org.springframework.web.context.ContextLoader - Root WebApplicationContext: initialization started
INFO : org.springframework.web.context.support.XmlWebApplicationContext - Refreshing Root WebApplicationContext: startup date [Sun Feb 12 13:50:17 IST 2023]; root of context hierarchy
INFO : org.springframework.beans.factory.xml.XmlBeanDefinitionReader - Loading XML bean definitions from ServletContext resource [/WEB-INF/spring/root-context.xml]
INFO : org.springframework.web.context.ContextLoader - Root WebApplicationContext: initialization completed in 713 ms
Feb 12, 2023 1:50:18 PM org.apache.catalina.core.ApplicationContext log
INFO: Initializing Spring FrameworkServlet 'appServlet'
INFO : org.springframework.web.servlet.DispatcherServlet - FrameworkServlet 'appServlet': initialization started
INFO : org.springframework.web.context.support.XmlWebApplicationContext - Refreshing WebApplicationContext for namespace 'appServlet-servlet': startup date [Sun Feb 12 13:50:18 IST 2023]; parent: Root WebApplicationContext
INFO : org.springframework.beans.factory.xml.XmlBeanDefinitionReader - Loading XML bean definitions from ServletContext resource [/WEB-INF/spring/appServlet/servlet-context.xml]
INFO : org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor - JSR-330 'javax.inject.Inject' annotation found and supported for autowiring
INFO : org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping - Mapped "{[/],methods=[GET],params=[],headers=[],consumes=[],produces=[],custom=[]}" onto public java.lang.String com.dev.spring.PersonController.listPersons(org.springframework.ui.Model)
INFO : org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping - Mapped "{[/remove/{id}],methods=[],params=[],headers=[],consumes=[],produces=[],custom=[]}" onto public java.lang.String com.dev.spring.PersonController.removePerson(int)
INFO : org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping - Mapped "{[/person/add],methods=[POST],params=[],headers=[],consumes=[],produces=[],custom=[]}" onto public java.lang.String com.dev.spring.PersonController.addPerson(com.dev.spring.model.Person)
INFO : org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping - Mapped "{[/edit/{id}],methods=[],params=[],headers=[],consumes=[],produces=[],custom=[]}" onto public java.lang.String com.dev.spring.PersonController.editPerson(int,org.springframework.ui.Model)
INFO : org.hibernate.annotations.common.Version - HCANN000001: Hibernate Commons Annotations {4.0.4.Final}
INFO : org.hibernate.Version - HHH000412: Hibernate Core {4.3.5.Final}
INFO : org.hibernate.cfg.Environment - HHH000206: hibernate.properties not found
INFO : org.hibernate.cfg.Environment - HHH000021: Bytecode provider name : javassist
INFO : org.hibernate.dialect.Dialect - HHH000400: Using dialect: org.hibernate.dialect.MySQLDialect
INFO : org.hibernate.engine.transaction.internal.TransactionFactoryInitiator - HHH000399: Using default transaction strategy (direct JDBC transactions)
INFO : org.hibernate.hql.internal.ast.ASTQueryTranslatorFactory - HHH000397: Using ASTQueryTranslatorFactory
INFO : org.springframework.web.servlet.handler.SimpleUrlHandlerMapping - Mapped URL path [/resources/**] onto handler 'org.springframework.web.servlet.resource.ResourceHttpRequestHandler#0'
INFO : org.springframework.web.servlet.DispatcherServlet - FrameworkServlet 'appServlet': initialization completed in 6245 ms
Feb 12, 2023 1:50:24 PM org.apache.coyote.AbstractProtocol start
INFO: Starting ProtocolHandler ["http-nio-8080"]
Feb 12, 2023 1:50:24 PM org.apache.catalina.startup.Catalina start
INFO: Server startup in [11813] milliseconds
Hibernate: select person0_.id as id1_0_, person0_.country as country2_0_, person0_.name as name3_0_ from PERSON person0_
Hibernate: insert into PERSON (country, name) values (?, ?)
Hibernate: select person0_.id as id1_0_, person0_.country as country2_0_, person0_.name as name3_0_ from PERSON person0_
 
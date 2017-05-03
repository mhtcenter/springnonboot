


Issues:
Filed to load class "org.slf4j.impl.StaticLoggerBinder".
	解决办法：
	在maven的slf4j的配置下增加：
	
	
			<dependency>
				<groupId>org.slf4j</groupId>
				<artifactId>slf4j-api</artifactId>
				<version>1.7.5</version>
			</dependency>
			<dependency>
				<groupId>org.slf4j</groupId>
				<artifactId>slf4j-log4j12</artifactId>
				<version>1.7.5</version>
			</dependency>
			
			

No appenders could be found for logger (org.springframework.test.context.junit4.SpringJUnit4ClassRunner).
	解决办法：
	main/resources下增加log4j.properties
	
	内容：
	# Root logger option
	log4j.rootLogger=INFO, stdout
	
	# Direct log messages to stdout
	log4j.appender.stdout=org.apache.log4j.ConsoleAppender
	log4j.appender.stdout.Target=System.out
	log4j.appender.stdout.layout=org.apache.log4j.PatternLayout
	log4j.appender.stdout.layout.ConversionPattern=%d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n	


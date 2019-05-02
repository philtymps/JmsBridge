# JmsBridge
JMS Bridge Utility - Bridge JMS Queues between each other or between file system and queue.

Usage:
   JmsBridge [-props:<properties_file>] [-save:<save_message_file>]
             [-test:<test_message_file>] [-verbose] [-help|-usage|-?]

	 -props:<properties_file>
		 Allows to specify the properties file name that contains jndi 
		 information about producer and consumer to set the jms bridge
		 between. If <properties_file> is not specified, this program
		 attempts to find and use '/jmsbridge.properties' on the root
		 of classpath.

	 -save:<save_message_file>
		 Indicates that incoming message should be just saved to a file
		 without being redirected to consumer. <save_message_file>
		 allows to specify the name of the file where the last incoming
		 message is be saved to. (Incoming messages do not get appended
		 to the save file so it contains the last received message only.

	 -test:<test_message_file>
		 Initializes connection to consumer only and sends a test text
		 message to it. The test message text is obtained from a file
		 specified by <test_message_file>.

	 -verbose
		 Runs in vervose mode (prints extra info on exceptions).

	 -help|-usage|-?
		 Outputs this usage information.

Example:
	 JmsBridge -props:bridge.properties
	 JmsBridge -props:bridge.properties -save:message.txt -verbose
	 JmsBridge -props:bridge.properties -test:TestMessage.txt



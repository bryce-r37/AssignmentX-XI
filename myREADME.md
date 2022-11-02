1.  The console logging level is set to INFO level in logger.properties, but file logging is set to the ALL level.
2.  This message comes from the default java Logger, which at the FINER level will check each JUnit test to see if it is disabled and prints this info before attempting to run that test. The message only appears twice because the logger has not been initialized before the first test is run.
3.  Assertions.assertThrows confirms that the called method throws an assertion, and that the assertion type thrown by that method call matches the given assertion type.
4.  1.  serialVersionUID is an identifier used to serialize or deserialize serializable objects. It helps us verify that a serialized object and the loaded class are compatible.
    2.  We have to override the default Exception constructors in order to include the serialVersionUID static data member in the TimerException object.
    3.  We don't override the other methods because the serialVersionUID is not used for any of the default Exception methods, so their default definitions and implementations are functional for the TimerException class.
5.  The static block initializes the static logger with the data found in logger.properties.
6.  .md (Markdown) file format files describe a directory, and bitbucket uses this format for their README files.
7.  The test is failing because a NullPointerException on Long timeNow is being thrown instead of a TimerException. timeNow is not initialized in this case because its initializer is located within a try block after an exception is thrown.
8.  The actual problem is that the logger messages are being printed even when the method throws an exception, but should only be printed when the method call is successful.
11. TimerException is a checked exception and NullPointerException is an unchecked exception thrown at runtime when a null pointer is accessed in place of an object.
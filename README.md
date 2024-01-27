# Java Threads README
## Author
Basma Mohammed (101187310)
## Course ID
SYSC 3303A - RealTime Concurrent Systems
## Assignment Description
The system that was designed and implemented is comprised of three barista threads and one coffee bean agent (supplier thread). Each barista continuously brews a cup of coffee and serves it. However, to brew and serve a cup of coffee, the barista requires three ingredients: coffee beans, water, and sugar. The agent thread has an infinite supply of all three ingredients. One of the baristas has an infinite supply of coffee beans, while another has water, and the third has sugar. The agent provides only two ingredients since each barista has an infinite supply of the third ingredient. The baristas' job is to brew 20 cups of coffee with the provided ingredients. 
## Available Files
- Counter.Java
- CounterTest.Java
## Code Explanation 
Counter.Java class explanation:
This class has two main methods provide_ingredients() and make_coffee(). 
- provide_ingredients(): selects two random ingredients from the list of 3 ingredients (coffee beans, water, and sugar) and then notifys other threads upon completion.
- make_coffee(): allows the barista with the third infinite ingredient to brew coffee by using the other two ingredients provided by the agent. The barista notifys other threads upon completion. 

CounterTest.java class explanation:
This class has two additional classes Agent and Barista classes. Both of these classes implement the Runnable interface since they are intended to be executed as a thread. CounterTest.java contains a main method that creates one agent thread and 3 barista threads which are all executed. 

## Running Instructions 
Run the CounterTest.java to execute all threads and observe the terminal window. 

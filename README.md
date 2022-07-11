# distributed-auction

**Requires Zulu11 JDK for Java 11.0.8**

The .jar files may be run either on the same computer or different computers within the same local network.

### instructions

1. Start the bank using the command "java -jar bank.jar portNumber" (port number must not already be in use)
2. Next, start one or more auction house(s) using the command "java -jar auctionHouse.jar portNumber bankHostName bankPortNumber" (port number must not already be in use, and different auction houses must operate on different port numbers)
3. Finally, start one or more agent(s) using the command "java -jar agent.jar bankHostName bankPortNumber"
4. Follow the on screen instructions as an agent

Once an item is bid on, a timer for 15 seconds starts. If no other valid bids are accepted, the agent with the highest bid will win the item at the end of the 15 seconds. If other bids are accepted, the timer will reset upon the valid bid being accepted.
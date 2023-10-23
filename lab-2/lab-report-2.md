# Lab Report 2 - Servers & SSH Keys 
## Part 1
#### StringServer Code: 
![image](stringserver.png)
#### Two Examples Using StringServer
![image](lab2sc1.png)
![image](lab2sc2.png)
* In both of these exmaples, the handleRequest method is called and the URL of the server is passed in.
* From there, the method ".getPath()" and ".contains()" get called to check the condition.
* Since the paths meet the condition (being "/add-message"), the url method ".getQuery()" gets called which retrives the query which in our exmaples are "helloguys" and the string of letters.
* After, the ".split()' method gets called which divides our query into a list between the '=' symbol. 

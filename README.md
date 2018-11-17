# Welcome to PlayerIO-jitterphysics
# - Documentation in how to use with PlayerIO in progress, you can copy paste this into your C# project, compile and it will work with PlayerIO.

This is an adaptation of jitterphysics to work with the awesome PlayerIO multiplayer services.
jitterphysics development looks to be quite abandon with better built-in solutions in game development tools like Unity.

My name is Oscar and I'm an indie developer, I'm the creator of Nukes of Bastion (For those interested http://www.nukes-of-bastion.com/) for Android and PC a few months back.

First of all thank you to PlayerIO for letting the world use your infrastructure and multiplayer solution free for up to 500 players, that's great for indie developers, and sure lets you grow your capabilities once you grow with your game and incomes, it was a top feature that made my mind on choosing work with you.

Over the last few months I was looking for a 2D Physics library over the web that would work with PlayerIO.
As you may already know, in order to put C# code into PlayerIO it must not use unsafe code , use static variables, or have any kind of reference to other .DLL external libraries, which many Physics libraries will heavily use.

Not only that, but the general advise from the community and PlayerIO staff is to use client side Physics, which IMHO this is a rather non-commercial advise, but I don't want this to be the main point of discussion and rather focus on the contribution background.

I couldn't follow that advise because I wanted to simulate Physics on both the client and the server, but the server being authoritative so synchronization and prediction could be used to smooth gameplay and prevent cheating at the same time, of course, such topics are another discussion, and even for that, I have created a neat library solution that lets you code in a single file for it to be used at both client and server solutions making it easier to code a multiplayer game.

After hundred of painful hours trying to adapt different open source 2D Physics engines to work with PlayerIO, the outcomes would be libraries working on PlayerIO with wrong results, or libraries simply too dependent on unsafe code or third party libraries to be feasible to use.

Then, I found Jitter Physics 2D port https://github.com/mattleibow/jitterphysics/, it didn't use unsafe code and was not dependent in third party libraries for mathematics but rather use it's own C# code for what it required, 

I spent several hours removing static variables and adapting code, and finally got it working.

# dispose-canonicus

.net c# Dispose pattern full implementation

# Motivation

After a recent refactoring of my really old code I want to use in one of my upcomming projects I've realized the errors of not implementing the Dispose method with the correct pattern.

I use many languages and tools all the time and I don't want to waste time to solve this again or look for it anywhere else, so I've decided to write this focused project that I can easily copy to any future project.

The only reasons I see one failing to implement the pattern are:
1. Not truly understanding the pattern in the first place
2. Consequently not being able to imagine the ramifications of not implementing it the correct way
- anybody that uses the code expecting it to work as if it implements the pattern correctly WILL create some bugs, and the cause might be hard to identify
- the advantages of the improper implementation of the pattern, to satisfy some requirements, in the end, are outweighed by the issues it creates by not going the route trusted by many
3. No support or cooperation from the team to use it and the lack of willingness to stick to the cause till the end

# Resources

Read the complete guide for implementing the dispose pattern is [here](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/implementing-dispose)

Go [here](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/unmanaged) for the context of using the pattern.

Making the Dispose method [idempotent](https://en.wikipedia.org/wiki/Idempotence) is a must.

[IUnknown interface](https://docs.microsoft.com/en-us/windows/win32/api/unknwn/nn-unknwn-iunknown) AddRef and Release pattern worked really well in c# for me to fine tune the allocation and deallocation of huge quantities of memory for live streams.
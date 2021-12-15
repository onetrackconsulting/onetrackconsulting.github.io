## Open Source

Open Source software is something I am very passionate about - I believe it is a huge productivity boon and in a lot of cases it can make sense to open source appropriately reusable features that you need for your application in order to have someone else maintain them.  I have a ton of experience as an open source user and have made contribution to a number of different projects but there are two projects that will always be kind of special to me:

### SquishIt (2010-present)

[SquishIt](https://www.nuget.org/packages/SquishIt) was one of the early asset optimization libraries for .net.  I initially submitted a bunch of platform-specific bug fixes to make it work with older versions of mono on linux, and from there became a core contributor and eventually kind of the only maintainer.  The main feature I introduced was a preprocessor pipeline that was configurable through code and allowed for a number of specific preprocessor contributions from the community.  I also split the package into multiple packages to allow easier use with disparate back ends like Nancy and got it to a stable 1.0 release.  The project is in maintenance mode at this point - tooling in .net core is good enough that I don't think it is worth carrying it into the "new world" so to speak.

### EdgeXFoundry (2020-present)
[EdgeXFoundry](https://www.edgexfoundry.org/) is a Linux Foundation project that provides both core services and microservice SDKs for building edge computing applications.  I originally got involved during the version 1.3 development cycle when it became clear a system that I inherited needed the ability to place its own messages on the bus established between services (in this case it was a 0MQ implementation that brings some technical difficulties into play).  The first PR I brought was to provide an API for background processes to send data through the messagebus trigger but I have continued working on it since.  Have submitted some small PR's to the go device SDK and core services but my main focus is on what we call the [application service SDK](https://github.com/edgexfoundry/app-functions-sdk-go).  Within that space I focus primarily on the interface to the service and have added a "custom trigger" API to the SDK that allows the wide range of customization I've needed to connect to various cloud and intermediate systems.
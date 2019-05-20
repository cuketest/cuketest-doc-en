## Frequent Asked Questions (FAQ)

<a id="version"></a>
#### Q: Which version of cucumber.js does CukeTest support?

**A**: CukeTest support Cucumber 5.x. "x" in the version number represent the almost latest version. We are upgrading engine periodically to newer version of Cucumber, so that CukeTest users can also work with new features of Cucumber.

<a id="testing_tools"></a>
#### Q: There are many test tools available on the market, such as Selenium, Appium, Calabash, etc. Which category does CukeTest belong to?

**A**: CukeTest is a test script editing and debugging platform that can integrate with multiple test frameworks as long as they support the JavaScript language. For example, Selenium and Appium test can be develop within CukeTest. CukeTest can be used to automate test for Web UI, API, mobile devices.

<a id="report_bug"></a>
#### Q: How can I report bugs or raise suggestions to CukeTest?

**A**: Report issues with one of the following methods:
* Submit issue on [github](https://github.com/cuketest/demos/issues)
* Open [Contact Us](http://www.leanpro.cn/contactus), submit your question and contact information.

<a id="sqllite"></a>
#### Q: How to use SQLLite3 in CukeTest?

I installed SQLLite3 and when I call it in CukeTest, I get the error "A dynamic link library (DLL) initialization routine failed. ... note_sqlite3.node."

**A**:  This is because SQLLite3 includes a dynamic link library that needs to be compatible at the binary interface level. The default installation with NPM is only compatible with Node, while CukeTest uses Electron. The binary level is not compatible, so it needs to be recompiled. The following link describes how to compile:

[https://stackoverflow.com/questions/32504307/how-to-use-sqlite3-module-with-electron](https://stackoverflow.com/questions/32504307/how-to-use-sqlite3-module-with-electron)

An easy way to do this is to download the binary for Electron directly from [https://github.com/zhangxy1035/electron_sqlite3](https://github.com/zhangxy1035/electron_sqlite3) and replace the corresponding ones in the appropriate directory. For CukeTest, it is the 32-bit version of Electron 2.0.9

<a id="fastfail"></a>
#### Q: There are dozens of scenarios in my scripts. If one scenario fails to execute, can I skip the rest scenarios quickly without running the them?

**A**: Yes, you can create a run configuration and set the "fast-fail" to "true", For more detail, check[Run Profiles](/execution/profiles.md)

<a id="embed_pictures"></a>
#### Q: My report has a lot of screenshots, it failed when generating the report, the error message is "Invalid string length"

**A**: You can set the screenshot save file to "stand-alone file" in Settings -> Reports. This way the report file will not become too big because of the screenshot.

<a id="commandline"></a>
#### Q: Can multiple projects be run together in series? For example, is it possible to string each run command through bat?

**A**: Yes, CukeTest supports command line mode. For specific commands, refer to [Command Line](/execution/cli.md)

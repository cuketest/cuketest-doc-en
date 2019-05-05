# CukeTest APIs

CukeTest provides several built-in NPM packages, each of which implements a category of automation APIs functionality. The API support are different on different platforms. The following table lists the capabilities of packages on each platform:

| Name | Functionality | Windows | Mac | Linux |
| :--- | :--- | :--- | :--- | :--- |
| cuketest | Automate CukeTest itself | Yes | Yes | Yes |
| leanpro.common | Utilities | Yes | Yes | Yes |
| leanpro.win | Windows Automation | Yes | No | No |
| leanpro.visual | OCR and Image | Yes | Partial | Yes |

## Package "cuketest"

There are a list of CukeTest APIs that you can use in test script. To use them, simply require the build-in "cuketest" module and then you will use them. You get intellisense when "require" them.

For example, the following code can be used to minimize the entire CukeTest UI window during the test, and then after the test restore the CukeTest window:

```javascript
const CukeTest = require("cuketest");
CukeTest.minimize();

//…the test operations to perform…

CukeTest.restore();
```

Here are the signature of the APIs:

* **delay\(milliseconds: number\)**

  To delay number of milli-seconds It returns Promise&lt;void&gt;, to use it in an async function, you can use “await” keyword, e.g. e.g. the following statement will delay a second:

  ```javascript
    await CukeTest.delay(1000);
  ```

* **minimize\(\)** Minimize the CukeTest window
* **maximize\(\)** Maximize the CukeTest window
* **restore\(\)** Restore CukeTest window to normal size.
* **launchProcess\(exePath: string, ...args: string\[\]\): child\_process.ChildProcess** Launch another process, return node.js ChildProcess object.
* **stopProcess\(proc: child\_process.ChildProcess\)** Stop the process, when pass in a ChildProcess object.

## Packages "leanpro.\*"

Packages prefixed with "leanpro." are the Automation API packages. See the [Node.js Automation API](https://github.com/cuketest/bdd-test-automation-with-cuketest/tree/ebf5a57e99e0b73dfad103a93f3cfd53548a2f0e/node_api/README.md) for details.


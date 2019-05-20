## Text Mode

CukeTest provides 2 editing modes when editing Gherkin file, Text Mode is explained in this page, and another is [Visual Mode](/features/visual_mode.md),

When you switch from Visual mode to Text mode, the Gherkin text in the document is automatically updated to reflect your change made in Visual mode.

In text mode, the UI will prompt you the keywords of Gherkin syntax when you type initial character. E.g. when you type `"F"`, it will prompt you `"Feature" `as intelli-sense.

In text mode, when you editing the Feature document, it will prompt you when there are any syntax errors. Some typical syntax errors can be:
* keywords are not spelled correctly, e.g. "Feature: " spelled as "feature: " or the colon is not followed the word.
* A Step (Given, When, Then) keyword followed feature title directly.
* In a document that designated to a certain language, still use English keyword. For example, if a Feature document specfied language to be Chinese using statement `"# language: zh-CN"`, however still use English keywords (e.g. Given, When, Then or Example). 

If you make some editing in the Text mode, you can switch back to Visual mode. During mode switch, CukeTest will check the syntax of the document, and if there are some invalid syntax in the document, the editor will prompt you the problematic line of the document. You have to fix the syntax first and then switch to Visual Mode.



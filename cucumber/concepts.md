# Cucumber Concepts  

<a id="bdd"></a>
## Behavior Driven Development (BDD)
BDD emerged from and extends TDD. Instead of writing unit tests from specification why not make the specification a test itself. The main idea is that business analysts, project managers, users or anyone without technical, but with sufficient business knowledge can define tests.

<a id="cucumber"></a>
## Cucumber
Cucumber is a testing framework that helps to bridge the gap between software developers and business managers. Tests are written in plain language based on the behavior-driven development (BDD) style of **Given**, **When**, **Then**, which any layperson can understand. Test cases are then placed into feature files that cover one or more test scenarios. Cucumber interprets the tests into the specified programming language and typically uses Selenium to drive the test cases in a browser. [more explanations](https://en.wikipedia.org/wiki/Cucumber_(software))


<a id="gherkin"></a>
## Gherkin
Gherkin is the language used to write specifications for Cucumber, Specflow and similar BDD frameworks. It is a business-readable, domain-specific language that lets you describe your software’s behavior without detailing how that behavior is implemented.
There are a few conventions:
- A single Gherkin source file contains a description of a single feature.
- Source files have the extension *.feature.
- There is a fundamental pattern to each Gherkin scenario, with a context: (Given), an event (When), and an outcome (Then)

You can read more about Gherkin here: <a href="https://github.com/cucumber/cucumber/tree/master/gherkin" target="_blank">https://github.com/cucumber/cucumber/tree/master/gherkin</a>


<a id="world"></a>
## Cucumber World
Please find more explanation in the below article
<a href="http://drnicwilliams.com/2009/04/15/cucumber-building-a-better-world-object/" target="_blank">http://drnicwilliams.com/2009/04/15/cucumber-building-a-better-world-object/</a>


<a id="feature"></a>
## Feature
Every `*.feature` file conventionally consists of a single feature. Lines starting with the keyword Feature: (or its localized equivalent) followed by three indented lines starts a feature. A feature usually contains a list of scenarios. You can write whatever you want up until the first scenario, which starts with Scenario: (or localized equivalent) on a new line.

<a id="scenario"></a>
## Scenario
Scenario is one of the core Gherkin structures. Every scenario starts with the "Scenario:" keyword (or localized one), followed by an optional scenario title. Each feature can have one or more scenarios, and every scenario consists of one or more Steps.


<a id="outline"></a>
## Scenario Outline
Copying and pasting scenarios to use different values can quickly become tedious and repetitive. Scenario Outlines allow us to more concisely express these examples through the use of a template with placeholders. The Scenario outline steps provide a template which is never directly run. A Scenario Outline is run once for each row in the Examples section beneath it (not counting the first row of column headers). The Scenario Outline uses placeholders, which are contained within `< >` in the Scenario Outline’s steps. 


<a id="background"></a>
## Background
Backgrounds allows you to add some context to all scenarios in a single feature. A Background is like an untitled scenario, containing a number of steps. The difference is when it is run: the Background is run before each of your scenarios, but after your "Before" hooks.


<a id="steps"></a>
## Steps
Scenarios consist of steps, also known as Givens, Whens and Thens.
Cucumber doesn’t technically distinguish between these three kind of steps. However, we strongly recommend that you do! These words have been carefully selected for their purpose, and you should know what the purpose is to get into the BDD mindset.

<a id="stepArg"></a>
## Step Argument
There are times when you want to pass a richer data structure from a step to a step definition.
This is what multiline step arguments are for. They are written on lines immediately following a step, and are passed to the step definition method as the last argument.

Multiline step arguments come in two flavors: **Table** or **Doc String**.

<a id="docstring"></a>
## Doc String
If you need to specify information in a scenario that won't fit on a single line, you can use a DocString. Multiline Strings (also known as DocString) are handy for specifying a larger piece of text. This is done using the so-called PyString syntax.
The text should be offset by delimiters consisting of three double-quote marks
`"""` on lines by themselves:

```gherkin

Scenario:
Given a blog post named "Random" with:
"""
Some Title, Eh?
===============
Here is the first paragraph of my blog post.
Lorem ipsum dolor sit amet, consectetur adipiscing
elit.
"""
```

<a id="table"></a>
## Table
Tables as arguments to steps are handy for specifying a larger data set - usually as input to a Given or as expected output from a Then. Here is the Example
```gherkin
Scenario:
  Given the following people exist:
    | name  | email           | phone |
    | Jason | jason@email.com | 123   |
    | Joe   | joe@email.com   | 234   |
    | Zark  | zark@email.org  | 456   |
```


<a id="example"></a>
## Example
Example is a data table that is placed under Scenario Outline, to provide data to the parameters in
Scenario Outline, for each line of data in Example table, the Scenario Outline will be executed once.

One Scenario Outline can have multiple Example tables, each Example table can be tagged independently, so that during the execution, you can run part of data using tags filter.

Below is an Example sample, placed inside the Scenario Outline:

```gherkin

Scenario Outline: eating
  Given there are <start> cucumbers
  When I eat <eat> cucumbers
  Then I should have <left> cucumbers

  Examples:
    | start | eat | left |
    |  12   |  5  |  7   |
    |  20   |  5  |  15  |
```

<a id="tag"></a>
## Tags
Tags are a great way to organize your features and scenarios. Consider this example:
```gherkin

@billing
Feature: Verify billing

  @important
  Scenario: Missing product description

  Scenario: Several products
```
A Scenario or Feature can have as many tags as you like, just separate them with spaces:
```gherkin
@billing @bicker @annoy
Feature: Verify billing
```
<a id="stepdef"></a>
## Step Definition
A step definition is analogous to a method definition / function definition in any kind of OO/procedural programming language. Step definitions can take 0 or more arguments, identified by groups in the Regexp (and an equal number of arguments to the Proc. Matching groups in the regular expression are passed as parameters to the step definition.

<a id="cucumber_expression"></a>
##Cucumber Expressions
Cucumber Expressions are simple patterns for matching Step Definitions with Gherkin steps.
Cucumber Expressions offer similar functionality to Regular Expressions, with the following improvements:
* Improved readability
* Custom parameter types
* Expression generation

Some more [explanations](https://docs.cucumber.io/cucumber/cucumber-expressions)

<a id="regex"></a>
##Cucumber Regular Expression
The regular expression in Step Definitions to match Step texts. Here are some [details](http://agileforall.com/wp-content/uploads/2011/08/Cucumber-Regular-Expressions-Cheat-Sheet.pdf)
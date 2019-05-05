# Walkthrough: Edit Feature File

This article demonstrates how to create a BDD [feature](../cucumber/concepts.md#feature) file in CukeTest "Visual" view. Below are the steps:

### 1. Create a feature file

Feature file is also called gherkin file, there are 2 ways to create a new feature file in CukeTest:

1. On CukeTest, select "File" -&gt; "New Feature", it will open a new feature file in editor.
2. On CukeTest, move mouse to "New Feature/Script" ![image](../.gitbook/assets/4_new_file_button.png) button on the toolbar, long press this button, it will shows you the dropdown menu list. Then click "feature" list item![](../.gitbook/assets/4_new_feature.png) ， a new feature file is also opened in editor.

### 2. Save feature file

Press key combination "Ctrl+S" \(⌘S on Mac\), or select "File" -&gt; "Save", file save dialog is opened, fill the file name and then save the file.

### 3. Compose feature file

In the software testing, test cases are created for product features. In Behavior Driven Development \(BDD\), test cases are written as scenarios, and they are stored in \*.feature file which follows the [gherkin](../cucumber/concepts.md#gherkin) format.

In CukeTest, you can write feature content in "Visual" view or in "Text" view.

### 4. "Visual" view

In "Visual" view, you can double-click any part of the text to make change to it. The following illustrates how to do it by creating a simple [Scenario](../cucumber/concepts.md#scenario).

### 5. Edit feature title

Move mouse to the feature title, double-click to make "\" editable, then you can change the title of this feature. For example, if want to write a feature to test "Calculator", you can change the title to be "Simple Calculation", then you press "Enter" key to move to the "Feature Description" field.

You can also double-click "" field to make it editable. Change the description to be "Test Calculator with simple math calculation".

### 6. Edit scenario

Click "Add new scenario" in "Visual" view, it will create a new empty scenario. Double-click "\" to make it editable, change the text to be "Addition". Then press "Enter" key to move to the next field, which is the first step.

On the first step, select keyword "Given" from the drop down, and change the text to be "I have a number 1".

Move to the second step, select keyword "When" and set step text to be "I add 1 to it"

Move to the third step, and set the keyword to be "Then" and set the text to be "I get result 2"

### 7. Edit in "Text" view.

Click "Text" button to switch to "Text" view of the editor, and you can edit the feature file in text mode.

For the feature you have just edited, switching to text view and you will see the following

```text
Feature: Simple Calculation
Test Calculator with simple math calculation

Scenario: Addition
Given I have a number 1
When I add 1 to it
Then I get result 2
```

If you are set CukeTest a language other than English, your feature file can also use the localized keywords in that language, make sure you add the language header in the feature file, so that parser can recognize the keywords correctly. For example, for Chinese language, the following header is `# language: zh-CN`

## Other Actions

There are some other steps you may perform, in order to edit your feature file:

### Add a new step

Two ways to add a new Step

1. Right click a step, it will shows step toolbar, right click "Insert Step" button to add a step before the current step.
2. Click "Add a Step" to add a new step at the bottom of the scenario.

### Delete a step

Right click the step, the step toolbox will show up, then click "delete" ![](../.gitbook/assets/delete_step.png) button to delete the step.

### Delete scenario

You can click the scenario title, on the context menu of the scenario, select "Delete Scenario" to delete this scenario.

You can also pop up this context menu by right click the scenario title.


# Gherkin

Gherkin document or Feature document end with \(.feature\). These 2 words are used interchangeably in this help document.

When you see "Feature", "Scenario", "Step", "Example" capitalized in the document, it is under the context of BDD or Cucumber, and referred specifically to the components in Gherkin document editing.

## Gherkin in Many Languages

Gherkin is available in many languages, allowing you to write stories using localized keywords from your language. In other words, if you speak French, you can use the word Fonctionnalité instead of Feature.

Keep in mind that any language different from en should be explicitly marked with a \# language: ... comment at the beginning of your \*.feature file:

```text
# language: fr
Fonctionnalité: ...
  ...
```

In CukeTest, you can convert Gherkin document from one language to the other, and the application will replace keywords with those in the target language. CukeTest can directly change gherkin document between English language and other language. If you want to convert language between other non-English documents, you need to first convert it from source language to English, and then from English to the target language. To convert the language of document, you can:

1. Switch to Text Mode for your feature document
2. Right click the editing area, and select "Convert language", then it will switch language between your configured default language and English.

If your configure default language is English, converting language won’t take effect.


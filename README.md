# Mufy-Regex-Tutorial-Demo
Complete Practical Source Code &amp; Zero-Basics English Tutorial for Mufy AI Rendering Regular Expressions, Kickstart Your New Exploration Journey.
Title: After some debugging, I'm preparing to open-source a project on GitHub. Please help me translate the following content into English.

---

README Homepage Introduction

Mufy AI Conversation Rendering Regex Zero-Basic Tutorial

What is Regex?
Regular Expression (regex for short) is a set of syntax rules used to match, search, and replace text patterns.
Simply put: it's a "text filtering template" for your computer to quickly extract content that matches a specific format from a large block of text.

What is Mufy?
Mufy AI is a mobile AI virtual character conversation platform (available on both Android and iOS), focusing on high‑freedom role‑playing and story interaction. Regex and HTML/CSS card rendering are its advanced features. This repository mainly covers the basics of regex usage in Mufy.

How to Use Regex (in General Mode)?

1. Regex Patterns
Based on basic regex knowledge, Mufy's regex can be written as <variable>([\s\S]*?)</variable>. For example: <smallphone>([\s\S]*?)</smallphone>.
If you need more advanced regex, you can ask an AI for help. However, note that Mufy is a simple AI chat app and does not have extra tolerance for complex regex setups, which may cause rendering failures.

2. Replacement String
The replacement string is what we actually need—the browser renders it via HTML/CSS to achieve our goal. If you use AI, just paste the code it gives you. However, problems often occur. Whether from the official documentation or AI‑generated code, triple backticks (```) are used during generation but are often filtered out by the browser or the app. If your code is not a continuous block, the backticks are essential; otherwise, the code may be correct but fail to render. You can use an AI like DeepSeek that allows copying the full text without ignoring rendered content. I have also released some of my own regex patterns in the Releases section. For the replacement string, I do not recommend directly using the official one, as it will likely cause rendering failure.

3. Testing
In the regex editing page, tap the "Test" button in the upper‑right corner to test your pattern. Note: this is the page for editing an existing regex, not the page for creating a new one.
After testing is complete, you can start normal conversations. To make the rendered text appear, simply let the AI finish its speech, then tap "Edit", and paste the regex pattern (just the short tag string, not the entire code, because you have already replaced the code with the regex) – the rendering effect will then appear.

4. Test Text
You can input test text, for example for smallphone:

```xml
<小手机>
  <状态>
    <电量>85</电量>
    <时间>14:30</时间>
    <信号>3</信号>
  </状态>
<小手机>
```

Be careful not to remove the xml declaration! Doing so will break your test text.

5. Special Cases
When rendering two pages simultaneously, you may choose to drop some elements—for example, you can remove the triple backticks mentioned earlier, and likewise the xml declaration. But removal depends on the situation! If your layers render correctly but there are things like /\html><$1?xml before or after the rendered layer that obstruct the view, you can delete them. If not, don't delete them. However, deletion might cause runtime issues, so proceed with caution.

6. Some Fun Examples
After your HTML renders correctly, you can enable browser storage permissions in the settings (on Android 13+, just enable image upload or text upload; if that doesn't work, grant storage permission). Then ask the AI to add a button that allows uploading images or files. After that, you can send images or files to your AI. You could even send an HTML file as an "app" to elegantly render another regex inside a single regex (essentially a workaround). Alternatively, you can place the regex "app" you want to render first, and the phone regex after, like this:

```
<gmail>([\s\S]*?)</gmail>
<小手机>
  <状态>
    <电量>85</电量>
    <时间>14:30</时间>
    <信号>3</信号>
```

This achieves rendering of two regexes at the same time! However, if you can use the format:

```
<variable1>dynamic content</variable1>
<variable2>dynamic content</variable2>
```

I recommend this approach, as it has a higher success rate.
During these processes, we notice—what if we upload an HTML that contains a URL and then open that URL? I can tell you clearly: it will navigate to the official website, and you have essentially opened a multi‑browser page inside Mufy's container! See the demonstration image below.
<img src="https://github.com/jiahao123666/Mufy-Regex-Tutorial-Demo/blob/main/Screenshot_20260621_172739.jpg?raw=true" width="650" alt="PICTURE">
---

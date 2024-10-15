
# Yooz Language

Yooz is a powerful and flexible AI-powered markup language designed to make chatbot interactions and data categorization seamless and intuitive. Yooz simplifies the process of creating conversational patterns for intelligent agents, making it easy to define responses based on keywords, patterns, and dynamic content replacement.


## Installation

To get started with Yooz, you can download the necessary libraries from the GitHub repository and integrate them into your project. Additionally, you can explore and test the functionality directly on the official website yooz.run. The website provides a user-friendly interface for experimenting with Yooz, allowing you to quickly see how the language operates and build your own interactive chatbots with ease.


## How Yooz Works

Yooz language allows developers to define **patterns**, **keywords**, **stop words**, **definitions**, and **data categorization** that control how a chatbot interprets and responds to user inputs. By parsing these components, Yooz creates a structured system that helps match user messages to appropriate responses. It utilizes a combination of exact matches, keyword detection, response templates, and dynamic parameter handling to ensure accurate and context-aware interactions.

## Features

- **General Definitions:** Define general terms using the `#` symbol.
- **Conversational Patterns:** Define question and response patterns with support for variables (`*1`, `*2`, etc.).
- **Stop Words:** Remove unnecessary words from user inputs.
- **Keywords:** Identify and respond based on a set of keywords.
- **Additional Responses:** Append multiple responses using `!>`.
- **Word Categories:** Define categories like pronouns and verbs and use them in patterns with `&`.
- **Support for Multiple Variables:** Use multiple variables in patterns and replace them in responses.

## Syntax Overview

The Yooz language is composed of different elements, including **definitions**, **patterns**, **keywords**, and **stop words**.

### 1. Definitions

Definitions are used to create variables that can be dynamically replaced in responses.

```yooz
#name : John Doe .
#country : Iraq .
```

### 2. Patterns

Patterns are used to match specific user inputs. The bot responses are defined after the pattern.

```yooz
(
    + How are you?
    - I'm doing great, thank you!
)
(
    + What's your name?
    - My name is #name .
)
```

### 3. Keywords

Keywords are used to create a more flexible response, where the chatbot can respond based on the presence of certain keywords in the input.

```yooz
(
    + {food, eat}
    - I love food! What's your favorite dish?
)
```

### 4. Stop Words

Stop words are ignored during input matching, which can help to ensure more accurate responses by excluding irrelevant words.

```yooz
- {the, a, an, of, in, on, with}
```

### 5. Dynamic Parameters

Dynamic placeholders allow responses to include specific parts of the user input. For example:

```yooz
(
    + My name is *1.
    - Nice to meet you, *1!
)
```

## Examples

### Example Input Code

```yooz
#name : AI Bot .
(
    + What's your name?
    - My name is #name .
)
(
    + I am feeling *1.
    - Why are you feeling *1?
)
- {I, you, he, she, it}
(
    + {hello, hi}
    - Hello! How can I assist you today?
)
```

### Sample User Messages and Responses

**User:** What's your name?  
**Bot:** My name is AI Bot.

**User:** I am feeling happy.  
**Bot:** Why are you feeling happy?

**User:** Hello  
**Bot:** Hello! How can I assist you today?

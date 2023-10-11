# Hinglish_Translator
This Python script acts as a Hinglish translator, converting English sentences into a mixture of Hindi and English. It uses the natural language processing capabilities of the NLTK library to recognize nouns in English sentences. Additionally, it uses the Google Translate API to translate languages.

# Approach
+**Noun Extraction (extract_nouns)**: Tokenize the English text, perform part-of-speech tagging, and extract nouns based on specific tags.

+**Translation (convert_to_hindi)**: Utilize the Google Translate API to translate English text to Hindi.

+**Noun Replacement (swap_nouns_hinglish)**: Identify English nouns, translate them to Hindi, create a mapping, and replace Hindi nouns in the original text.

+**Usage in the Code**: Collect user input, translate it to Hindi, and replace nouns to generate the final Hinglish sentence.

This script showcases a straightforward approach to translating English sentences to Hinglish, maintaining the structure while incorporating translated nouns.

# Prerequisites
Make sure you have the necessary Python libraries installed before running the script. You can enter the following commands.

+pip install nltk

+pip install googletrans==4.0.0-rc1

# Import Statements

import re

import nltk

from nltk import pos_tag, word_tokenize

from googletrans import Translator as LanguageTranslator

+**re**: Regular expression module for text pattern matching.

+**nltk**: Natural Language Toolkit library for text processing.

+**pos_tag**, word_tokenize: Functions for part-of-speech tagging and word tokenization.

+**Translator**: Google Translate API wrapper for language translation.


# Usage
A set of three functions implements the basic script function.
1. **extract_nouns(text)** - Identifies nouns in a given English text.
   Input: English text.
   Output: List of identified nouns.
2. **convert_to_hindi(text)** - Translates text to Hindi using the Google Translate API.
   Input: English text.
   Output: Translated text in Hindi.
3. **swap_nouns_hinglish(hindi_text, english_text)** - Identifies nouns in the English text, translates them to Hindi, and replaces them in the Hindi text.
   Inputs: Hindi text and its corresponding English text.
   Output: Hinglish text with translated nouns.
To demonstrate how it works, the script provides a simple user interface that asks users to input an English sentence. The text then translates the sentence into Hinglish and displays the result.

# Example
For example
Here is an example of how to use the script.

#Get user input and test the functions

user_input = input("Enter a sentence: ")

hindi_translation = convert_to_hindi(user_input)

result_hinglish = swap_nouns_hinglish(hindi_translation, user_input)

#Display the result

print("Hinglish Sentence:", result_hinglish)

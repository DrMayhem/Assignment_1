# Hinglish_Translator
This Python script acts as a Hinglish translator, converting English sentences into a mixture of Hindi and English. It uses the natural language processing capabilities of the NLTK library to recognize nouns in English sentences. Additionally, it uses the Google Translate API to translate languages.

# Prerequisites
Make sure you have the necessary Python libraries installed before running the script. You can enter the following commands.

pip install nltk

pip install googletrans==4.0.0-rc1

# Usage
A set of three functions implements the basic script function.

1.remove_name (text).
This function takes English text as input and uses the NLTK library to display the ideas in the text. It uses phrase markers to recognize words with noun markers.

2.Translation_to_Hindi (text).
This service uses the Google Translate API to translate the data from English to Hindi. It initializes the translation instance and requests a translation from the source language ('en') to the destination language ('hi').

3.swap_nouns_hinglish(Hindi_text, English_text)
The basic semantic logic is used in this work. First, it uses extract_nouns to extract the nouns in the English text. Then, it translates this English name to Hindi using convert_to_hindi. Finally, it replaces the corresponding nouns in the Hindi text with their English equivalents.

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

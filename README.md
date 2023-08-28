def analyze_sentence(sentence):
    sentence_length = 0
    word_count = 0
    vowel_count = 0

    for char in sentence:
        sentence_length += 1

        if char == ' ':
            word_count += 1

        if char.lower() in 'aeiou':
            vowel_count += 1

    # Adjust the word count by adding 1 since the last word doesn't have a space after it
    word_count += 1

    return sentence_length, word_count, vowel_count


# Example usage
input_sentence = "This is an example sentence."
length, words, vowels = analyze_sentence(input_sentence)

print("Sentence length:", length)
print("Number of words:", words)
print("Number of vowels:", vowels)

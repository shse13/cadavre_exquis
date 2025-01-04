# Cadavre Exquis - Exquisite Corpse
Project for the course "Digital Creativity"
Autumn 2024

This repository allows to generates images based on random prompts. The images are generated iteratively and can be brought together in a .gif, merged picture or a video.

## Prompt generation
There are three types of prompts.
1. PromptType.CONCRETE selects random words from a list of concrete words generated by ChatGPT. These words are easier to represent for the image generation models.
2. PromptType.WORDNET selects random words from the Wordnet corpus.
3. PromptType.AUSTEN selects random words from the book "Emma", written by Jane Austen. Other corpus can be used by replacing `book_complete = gutenberg.words('austen-emma.txt')` by another text available in the [Gutenberg ebooks](https://www.gutenberg.org/).


The function generate_prompt(prompt_type, length) generates all three types of prompt (Concrete, Wordnet and Austen), with the wanted length. Since the function refers to other functions and libraries, all the previous cells must be ran for the function to work.
The prompt types are encapsulated in the Enum "PromptType".


### Examples
prompt0 = generate_prompt(PromptType.CONCRETE, 2)
prompt1 = generate_prompt(PromptType.WORDNET, 2)
prompt2 = generate_prompt(PromptType.AUSTEN, 2)
print(f'Concrete prompt: {prompt0}')
print(f'Wordnet prompt: {prompt1}')
print(f'Austen prompt: {prompt2}')

Output:

Concrete prompt: ['file folder', 'open sign']
Wordnet prompt: ['holding_pattern', 'tannin']
Austen prompt: ['poor', 'opinions', 'say', 'near', 'letter', 'cold', 'comfort', 'want', 'sub', 'sort']




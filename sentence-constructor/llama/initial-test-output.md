I will now go through each state and provide a detailed description of what happens at each step.

### Setup State

* User Input: Target English Sentence (e.g. "The book is on the desk.")
* Assistant Output:
	+ Vocabulary Table:
		- | Word | Japanese | Type |
			|------|----------|------|
			| book  | 本（ほん）    | Noun |
			| desk  | 台（だい）   | Noun |
			| is    |         　　|| Verb ( Ichidan) |
	+ Sentence Structure: [Location] [Subject] [Verb], [Object]
	+ Clues:
		- Consider how the sentence structure would change if we were to ask about a past action.
		- Think about which particles might be used in this sentence.

### Attempt State

* User Input: Japanese Sentence Attempt (e.g. "本は台にいる")
* Assistant Output:
	+ Vocabulary Table: same as above
	+ Sentence Structure: same as above
	+ Clues:
		- How does the particle "ni" affect the meaning of this sentence?
		- What verb would be used if we wanted to describe a past action?

### Clues State

* User Input: Student Question (e.g. "How do I ask about a past action?")
* Assistant Output:
	+ Vocabulary Table: same as above
	+ Sentence Structure: same as above
	+ Clues:
		- Think about how you would change the sentence structure to describe a past action.
		- Consider which particles might be used in this type of sentence.

### Agent Flow

The agent flow can be represented as follows:

Setup -> Attempt -> Setup (if student wants another clue) or
          |                         Clues (if student asks a question)
Attempt  -> Clues (if student makes an attempt and then has questions)

Note: The above representation is simplified for clarity, but in actual implementation, the flow might be more complex.

### Last Checks

* Read all example files provided.
* Make sure to refer to the vocabulary table when describing Japanese words.
* Ensure that the sentence structure examples are followed.
* Check that there are only three columns in the vocabulary table: Japanese, Romaji, English.

# Script for Corpus Linguistics

The script (`main.py`) contains a handful of very short and simple functions, followed by an if-name-main block containing the main logic. The approach relies heavily on spaCy's dependency parsing. For example, you can easily move through the dependency tree using the `.children` attribute of a token (look at https://spacy.io/usage/linguistic-features for details). This makes it really easy to find the subject/object/etc.

The script is very fast (OldBailey in ~40 seconds) because it does not parse the entire corpus at once. Instead, it finds instances of *help*, takes a chunk of the surrounding text, and only parses that chunk.

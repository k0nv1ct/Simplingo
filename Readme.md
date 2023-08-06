# SimpLingo

This project focuses on simplifying English sentences and documents based on the Common European Framework of Reference (CEFR) difficulty levels of words. The goal is to make text more accessible to readers with varying language proficiency levels. The project comprises two phases: identification of words with their respective CEFR levels and simplification using fine-tuned models.

## Phase 1: CEFR Word Tagging

In the first phase, words are tagged with their corresponding CEFR levels (A1, A2, B1, B2, C1) to indicate their difficulty. The tagging process is achieved as follows:

1. **Web Scraping Common Words**: A list of common words belonging to different CEFR levels is compiled through web scraping.
2. **Tagging Tokens**: The dataset, specifically the CoNLL-2003 dataset, is used for tagging tokens with their CEFR levels. Words from the common word list are used to tag tokens, and any words not in the dictionary are tagged based on their frequency of appearance.
3. **CEFR Level Assignment**: Words that appear more than 90% of all tokens are tagged as C1, more than 70% as B1, more than 80% as A2, more than 50% as B2, and less than 30% as C1.

## Phase 2: Sentence Simplification

The second phase involves sentence simplification using a fine-tuned BERT Uncased model. The steps are as follows:

1. **Test Run**: The newly tagged dataset is utilized for a test run with the fine-tuned BERT Uncased model.
2. **Results Demonstration**: The outcomes of the test run are showcased in a Jupyter Notebook, providing insights into the effectiveness of the simplification process.
3. **Meaning and Usage Extraction**: For challenging words, a dictionary approach is planned. This involves using tools like the NLTK synsets dictionary or PyWin dictionary to retrieve meanings and usages of difficult words.

## Future Work: Complete Phase 1

The upcoming phase of the project will involve tagging words from a larger corpus such as OpenOrca or Falcon RefinedWeb. This expanded tagging process aims to further enhance the accuracy of CEFR level assignments. Following this, a Falcon 7B model will be trained using the extensively tagged data.

## License

This project is open-source and is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute this project in accordance with the terms of the MIT License.

## Contributions

Contributions to the project are welcomed and encouraged. If you find any issues, have suggestions for improvements, or want to collaborate, please feel free to submit pull requests or raise issues in the project repository.

## Acknowledgments

We acknowledge the support of open-source tools and resources, including the CoNLL-2003 dataset, BERT Uncased model, NLTK, PyWin, and other libraries that have contributed to the success of this project. Special thanks to the community for its continuous encouragement and feedback.

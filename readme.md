# TripTeller

Automated Travel Guide Writer

This program uses OpenAI's GPT-3.5 and DALL-E to generate an entire travel guide book for each town listed in the `towns.csv` file. Each town's travel guide will have a preset list of chapters that GPT-3.5 will use to write the entire chapter. After all chapters are finished, they will be combined into a `.docx` file and DALL-E will provide images for each chapter.

![preview_redd_it-ehv4tdctj6sa1](https://user-images.githubusercontent.com/36016088/230405200-0b0e9af3-2408-4243-9bd2-ec7d43be78bd.png)

## Installation
1. Clone this repository
```
git clone https://github.com/nitebyte/TripTeller.git
```
2. Install the required modules:

   - `openai`
   - `ebooklib`
   - `docx`
   - `requests`
   - `json`
   
3. Get an OpenAI API key [here](https://beta.openai.com/signup/).
4. Replace the `api_key` in the `PR` function and the `headers` dictionary with your OpenAI API key. Lines 18, 19, and 95.
5. Run the program with the command:
```
python TripTeller.py
```
6. Your completed travel guide book(s) will be saved as a `.docx` file in the same directory.


## Usage
1. The `towns.csv` file contains a list of towns in the format `Town,State`.
2. Each town will have its own `.txt` file that contains the generated text for its travel guide.
3. After running the program, the generated travel guide for each town will be saved as a `.docx` file in the same directory.
4. To add or modify chapters or sections, edit the `book` variable in the `TripTeller.py` file.
5. To change the number of tokens GPT-3.5 uses, modify the `token` parameter in the `PR` functions.
6. To change the size of the images that DALL-E generates, modify the `data` dictionary in the `txt_to_docx` function.


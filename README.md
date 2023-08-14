# DocumentDiglet

Project: Offline Semantic Document Search 

*Note this description is outdated as of 8/14. Will make an update soon.

This project aims to create an efficient, offline way to semantically search documents. It offers a streamlined approach to make any dynamic repository easily accessible to team members, surpassing the capabilities of simple keyword search functionalities like Ctrl+F or an FAQ.

By leveraging transformer models and cosine similarity, this project provides the ability to 'converse' with your documents, initiating an interactive and intelligent text exploration.

The project enhances privacy as it operates completely offline, ensuring no data is shared with external entities. It offers a unique combination of intelligent document retrieval and stringent data privacy.
About Semantic Matching Transformers

Transformers are a type of deep learning model that uses attention mechanisms to capture the context of words in a text and generate high-quality sentence embeddings. A 'semantic matching transformer' is trained to understand the semantic similarity between sentences.

In this project, we're using the 'all-MiniLM-L6-v2' model from Hugging Face's model repository. MiniLM is a size-efficient transformer model that retains considerable language understanding capabilities. The 'all-MiniLM-L6-v2' model is specifically fine-tuned for creating sentence embeddings that can be compared for semantic similarity.
Requirements

    Python 3.9 or newer.
    MongoDB. If not already installed, follow the instructions at MongoDB's official documentation.

Installation and Setup

    Download the Semantic Transformer Model:

    This project uses the 'all-MiniLM-L6-v2' transformer model to create sentence embeddings. You can download the model from the Hugging Face Model repository.

    Create a virtual environment (Optional but recommended):
        Using venv: python -m venv myenv (You may need to use python3 instead of python depending on your system setup.)
        Using conda: conda create -n myenv python=3.9

    Activate the virtual environment:
        Using venv:
            Windows: myenv\Scripts\activate
            Linux/MacOS: source myenv/bin/activate
        Using conda: conda activate myenv

    Install required Python packages:
        PyQt5: pip install pyqt5 or conda install -c anaconda pyqt
        nltk: pip install nltk or conda install -c anaconda nltk
            After installation, run the Python interpreter and execute: import nltk; nltk.download('punkt'); nltk.download('stopwords')
        pymongo: pip install pymongo or conda install -c anaconda pymongo
        sentence-transformers: pip install sentence-transformers or conda install -c conda-forge sentence-transformers
        numpy: pip install numpy or conda install -c anaconda numpy
        shutil (standard library in Python, no need to install separately)
        subprocess (standard library in Python, no need to install separately)

    Prepare the Learning Data:

    Create a plain text file named learnings.txt. Place this file in the appropriate directory based on your script's configuration. This file will be used to populate the knowledge base.

Please adjust file and directory paths in the script as needed for your system setup.

Usage

Run the GUI script in your virtual environment:

python gui_script.py

The main interface includes an input line, several buttons for performing different commands, and a response box to view the results. Here is a brief rundown of what each part does:

    Input Line: Enter your query or command here.

    Response Box: The results of your query or command will appear here.

    Dig Button: Executes the 'ask_command' function from the main script with the query entered in the input line.

    Reveal Button: Executes the 'reveal_command' function from the main script with the query entered in the input line.

    Eliminate Button: Executes the 'eliminate_command' function from the main script with the query entered in the input line.

    Update Button: This is linked to two input lines labeled 'Original Content' and 'New Content'. The function 'update_command' is executed with these two input values as arguments.

    Search Button: Executes the 'search_command' function from the main script with the query entered in the input line.

    Refresh Button: Executes the 'compute_and_store_embedding_and_backup_learnings' function from the main script, which updates the data.

Please refer to the 'DocumentDiglet_NoInterpy_V5' script documentation for a more in-depth description of what each command does.
Contributing

We welcome contributions from the community. Please read our contribution guide before making a pull request.
License

This project is licensed under the Apache license 2.0 - see the LICENSE.md file for details.
Acknowledgments

The 'Document Diglet' was developed by IMNMV & GPT-4.

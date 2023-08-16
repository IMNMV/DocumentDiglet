The Document Diglet project is an offline program to search and retrieve specific sections of documents. Imagine having the ability to converse with your repository, asking complex questions, and receiving relevant excerpts in return.

At the core of this system, we're employing the MS MARCO Distillbert v4 model from Hugging Face (https://huggingface.co/sentence-transformers/msmarco-distilbert-base-v4). This model, designed specifically for information retrieval tasks, enables the creation of rich sentence embeddings that encapsulate the meaning and context of the text.

By utilizing the sentence transformers library, Document Diglet processes the content of a document, breaking it down into sentences or sections, and computes corresponding embeddings for each part.

When a user issues a query or prompt, the system calculates the cosine similarity between the query's embedding and the embeddings of all stored sections. The top-matching sections, based on similarity, are returned to the user.

Unlike many other semantic search tools that rely on cloud-based models and APIs, Document Diglet operates entirely offline. This ensures complete privacy and control over your documents.
The system is designed to adapt to continually changing repositories, allowing team members to add, modify, or delete content as needed. This makes it suitable for a wide range of applications, from internal knowledge bases to personal document management within a simple GUI

Document Diglet adds the next step to traditional search functionalities like Ctrl+F by offering semantic understanding. It doesn't just look for exact keyword matches; it understands the meaning behind your query and finds the most relevant sections, even if they are phrased differently.

Framework and Architecture

The front-end Graphical User Interface (GUI) of the Document Diglet project is constructed using the PyQt5 library. This framework facilitates the creation of an interactive and responsive user interface.
User Interaction Management

The GUI is equipped with specialized functionalities to manage user interactions:

    Query Handling: Functions such as handle_ask_button, handle_reveal_button, handle_search_button, and related handlers are devised to process various types of user queries and return pertinent excerpts.
    Error Management: The handle_error function ensures robust error capture and notification, contributing to system stability.
    Auxiliary Controls: Additional functions like handle_refresh_button, handle_help_button, and handle_bug_report_button provide supplementary controls for refreshing content, accessing help, and reporting bugs.

Database Integration

The GUI's integration with MongoDB is manifested through several key functions:

    Connection Management: The toggle_mongodb function provides the ability to activate or deactivate the MongoDB connection, illustrating flexibility in database connectivity.
    Collection Handling: Functions such as get_db_collection, update_last_used_collection, and get_last_used_collection facilitate meticulous management of database collections.

Dynamic Responsiveness

The GUI's dynamic responsiveness is evident in its ability to adapt to repository changes. Features such as the handle_refresh_button function support this adaptability.
Privacy and Security Considerations

The offline operation of the GUI ensures user privacy and data integrity. Security-related functions like close_mongodb_if_active reflect the GUI's adherence to secure practices.

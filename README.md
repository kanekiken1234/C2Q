# C2Q
Context to Questions Generation System


# Abstract:
In courseware business, creating Assessment Questions automatically from a given
Shared Stimulus is in high demand. This will reduce the overall manual cost & effort
significantly. Question answering is a very popular task in Natural language processing.
Question generation has a lot of use cases with the most prominent one being the ability
to generate quick assessments from any given content. We built an AI tool based on Text
Mining that will have the capability to understand the shared stimulus and then generate
different types of assessment content as per requirement.

# Design:
We decided to build a Web Application, with a Server that manages API calls from the
Web Application and the Question Generation Engine.
High Level Description:
1. User must write / upload a text document on the Web Application and choose the
type of question that has to be generated. After clicking on the “Generate” button,
an API call is made to the server. The API call prompts two things:
a. If a file has been uploaded, it makes the sever save the text file in its file
storage
b. If text has been provided, it makes the server create a text file, write the
content in it and name the file with cryptographical strong pseudorandom
string of length 10.
2. The API call returns the file name to the Web App in response. The Web app shows
the file name in pending section.
3. Then the server initializes the Question Generation Engine with 2 important
parameters, the text file and the type of question that has to be generated. Then the
model runs.
4. It starts predicting respective questions and answers of the type mentioned by the
user and writes them in the database in form of a document.
5. As soon as a document is inserted in the database, server is informed about the
change, it gets the document that has been inserted and sends it to the Web App.
6. The Web App then shows the status of the pending file as completed file.
7. User can now use the file name to fetch the document of Questions and Answers and
download it on their local file system as a text file.

# Source Code:
LINK -> https://drive.google.com/drive/folders/1uKembVa84yhnWWEzCcgE9rYmBsKVeqyc?usp=sharing

# Python-Quiz

## Here's how it works

The game is very simple. There will be three randomly generated quiz questions, from a question bank I have created. The user has to try and get them right. However, there is a slight twist as all the questions are opinionated, so the answer may not always be what they think. 

The game will greet the user and then ask for their name. From there, the quiz starts. The three random questions will be shown one after the other. The quiz will let them know immediately if their answer is correct or not through a congratulatory or commiserative message respectively. At the end their total score will be produced and they will receive a medal based on how many they got right. There is no medal for those who get no correct answers. Thereafter, the game ends and a leaving message is displayed.


## Some technical information on the code

The initial greeting uses a simple print function and displays a welcome message. Then there is an input function to gather the name of the user. The user's name is then stored in u_name and used to create a starting message, again displayed through a print function.

The questions for the game are called randomly from the module random_question. This is done through the get_question function which picks questions at random from my list of tuples, due to the return random.choice(questions). 

Then a for loop is used to make sure the same code is run three times, so that three questions are produced. The first part of each tuple is the question and the second part is the answer. So the first part is used under the 'q' (for question) variable, the question (q[0]) is displayed, and the answer is captured using the input function. The user then inputs their answer and if it matches the answer in the second half of the tuple q[1] then a congratulatory message is displayed using the print function. Otherwise it displays a commiserative message instead. This is done through an if statement. The score counter also goes up if the answer is correct. After the three questions have been asked, the score is displayed along with a message based on the score. This was again done with if/elif statements. The final greeting is personalised using the u_name variable from earlier and after displaying this, the quiz comes to an end.

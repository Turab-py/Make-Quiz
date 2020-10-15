# Make-Quiz
How to make a quiz in python 3.
users = dict()

def signup():
  global users

  name = input(str("Enter your name: "))
  password = input(str("Enter your password: "))
  users[name] = password


def login():
  global users
  name = input(str("Enter your name: "))
  if name in users.keys():
    print ("Correct! ")
    password = input(str("Enter your password: "))
    if password in users.values():
       
        print ("Correct! ")
    else:
        print ("Password is incorrect!")
  else:
    print ("your user name is not present! ")
 
  users[name] = password

def creating_a_qiuz():
    questions = {
    "What is the capital of Pakistan? ":{"correct":"b", "answers":['Karachi','Islamabad','Lahore','Peshawar']},
    "Two sum two makes? ":{"correct":"b", "answers":['three','four','two','one']},
    "Who was the founder of AI? ":{"correct":"d", "answers":['Newton','Einstein' ,'John McCarthy','Alan Turing']},
    "What is the father of programming? ":{"correct":"c", "answers":['Steven Hawking','Dalton','Dennis Ritchie','Dr. Abdul Salam']},
    "Two cube root three makes? ":{"correct":"b", "answers":['four','eight','sixteen','thirty two']},
    "Ali is a _____ boy. ":{"correct":"c", "answers":['bad','dirty','good','brave']},
    "Hazrat Mohammad SAW is our _____ Prophet? ":{"correct":"b", "answers":['First','Last','Second','Second last']},
    "Hazrat Ali A.S is our ___________ Caliph? ":{"correct":"a", "answers":['fourth','eighth','sixteenth','third']},
    "Four cube root two makes? ":{"correct":"b", "answers":['four','sixteen','thirty two','eight']},
    "Who was Stephen Hawking? ":{"correct":"d", "answers":['Rider','Doctor','Engineer','Scientist']}
    }  

    anslabels = ['a','b','c','d','e']
    correct = 0
    total = len(questions)
    input("\nThank you for trying out William Passmore's Python 3 Quiz!\nPress ENTER to start!\n")
    for k, v in questions.items():
        print(k)
        x = 0
        for ans in v["answers"]:
            print(anslabels[x] + ": " + str(ans))
            x += 1
        answer = input("\nType a, b, c, d to select your answer. Then press ENTER.\n")
        if(answer == v["correct"]):
            correct += 2
        print("\n")
    score = str((correct / total) * 100) + "%"
    print("Quiz Complete!\nYour score is " + score + " on this quiz.")
    

def quiz():
    signup()
    login()
    creating_a_qiuz()
   
quiz()

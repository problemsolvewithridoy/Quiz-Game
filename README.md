
# Quiz Game using basic python

This is a Quiz Game project developed in Python. The game is designed to test the knowledge of the players on various topics such as history, geography, science, etc. It is a beginner-friendly project, which can be used by anyone who wants to learn and practice basic programming concepts in Python.

The Quiz Game has a user-friendly interface, which makes it easy to play. The game consists of a series of questions, and the player has to choose the correct answer from the given options. The player's score is displayed at the end of the game, and the game can be played multiple times to improve the score.

The code for this project is well-commented and easy to understand. It can be used by anyone who wants to learn how to create a simple quiz game in Python. The code can also be modified to add new questions, topics, or features.

Feel free to download, use, and modify the code to suit your needs. Happy coding!

To make this project you need to follow this step:-










## Installation

Install package with pip

```bash
  pip install logging

```
    
## Deployment

To deploy this project run

```bash
import time
import logging

logging.basicConfig(filename = "Quiz_game.log", level = logging.DEBUG, format = ("%(asctime)s %(levelname)s %(message)s"))


# Make function for loading 
def sleep_time():
    print("Loading your question paper", end="")
    a = 0
    while a<100:
        print(".", end="")
        time.sleep(0.05)
        a+=1
    return " "
try:
    # for make a result
    ok = 0
    ng = 0
    wrong = []

    # check you are intersted or not
    ans = input("Are you ready to play Quiz Game? ").lower()

    if ans != "yes":
        print("Thank You")
        logging.info("user aren't ready to play Quiz Game")
        pass
    # take user information
    else:
        logging.info("user ready to play")
        name_list = []
        name = input("Please Give Your Name: ")
        logging.info("user name is: %s", name)
        name_list.append(name)
        mobile = input("Please Give Your Mobile Number: ")
        logging.info("user mobile number is: %s", mobile)
        name_list.append(mobile)
        age = input("please Give Your Date of Birth: like dd/mm/yy ")
        logging.info("user birth day date is: %s", age)
        name_list.append(age)

        print("\n" + "="*57 + " Thank You " + "="*57)

        print(f"""
    Your Name is:          {name_list[0]}
    Your Mobile Number is: {name_list[1]}
    Your Date of Birth is: {name_list[2]}     
        """) 
        ask = input("is everything correct? ")

        if ask != "yes":
            print("please try again")
        else:
            print("Creating your Gameing ID ", end="")
            a = 0
            while a<102:
                print(".", end="")
                time.sleep(0.05)
                a+=1
            #return " "
            print ("\n\n" + f"Your Quiz Gameing ID is: {name_list[0][0] + name_list[1][1::2] + name_list[2][-4::1]}")
            
            user_id =  name_list[0][0] + name_list[1][1::2] + name_list[2][-4::1]
            
            logging.info("user Quiz Gameing ID is: %s", user_id)

            time.sleep(2)
            print("\n" + "="*53 + " Let's start the Game " + "="*52)

            print("""

    Please Select the Subject 🙂

    1. Science
    2. Robotics
    3. Math
    4. Computer
    5. Sports
                """)
            sub = input("please choose one: ").lower()
            
            logging.info("user choosed %s no subject", sub)

            if sub == "1" or sub == "science":
                    print("\n"+"="*47 + " Thank you for selected Science " + "="*47)
                    sleep_time()

    #Question 1
                    q1 = input("""1. Which of the following is used in pencils?
    a) Graphite
    b) Silicon
    c) Charcoal
    d) Phosphorous
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "a" or q1 == "graphite":
                        ok += 1
                    else:
                        ng +=1
                        wrong.append(f"""1. Which of the following is used in pencils?
    a) Graphite
    b) Silicon
    c) Charcoal
    d) Phosphorous

    Correct ans is:- a)Graphite
    you gave: {q1}
    """)

    # Q2 for Science
                    q2 = input("""2. Chemical formula for water is
    a) NaAlO2
    b) H2O
    c) Al2O3
    d) CaSiO3
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "b" or q2 == "h20":
                        ok += 1
                    else:
                        ng += 1
                        wrong.append(f"""2. Chemical formula for water is
    a) NaAlO2
    b) H2O
    c) Al2O3
    d) CaSiO3

    Correct ans is:- b)H2O
    you gave: {q2}
    """)

    # Q3 for Science
                    q3 = input("""3. The gas usually filled in the electric bulb is
    a) Nitrogen
    b) Hydrogen
    c) Carbon Dioxide
    d) Oxygen
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "a" or q3 == "nitrogen":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. The gas usually filled in the electric bulb is
    a) Nitrogen
    b) Hydrogen
    c) Carbon Dioxide
    d) Oxygen

    Correct ans is:- a)Nitrogen
    you gave: {q3}
    """)

    # Q4 for Science
                    q4 = input("""4. Which of the gas is not known as green house gas?
    a) Methane
    b) Nitrous oxide
    c) Carbon dioxide
    d) Hydrogen         
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "d" or q4 == "hydrogen":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. Which of the gas is not known as green house gas?
    a) Methane
    b) Nitrous oxide
    c) Carbon dioxide
    d) Hydrogen         

    Correct ans is:- d)Hydrogen
    you gave: {q4}
    """)

    # Q5 for Science
                    q5 = input("""5. Which of the following is used as a lubricant?
    a) Graphite
    b) Silica
    c) Iron Oxide
    d) Diamond           
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "a" or q5 == "graphite":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. Which of the following is used as a lubricant?
    a) Graphite
    b) Silica
    c) Iron Oxide
    d) Diamond           

    Correct ans is:- a)Graphite
    you gave: {q5}
    """)
            elif sub == "2" or sub == "robotics":
                    print("\n" + "="*47 + " Thank you for selected Roborics " + "="*47)
                    sleep_time()

    #Q1 for robotics
                    q1 = input("""1. What is the full meaning of IR sensor?
    a) infrared
    b) infrared light
    c) international radio
    d) internet refollow
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "a" or q1 == "infrared":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. What is the full meaning of IR sensor?
    a) infrared
    b) infrared light
    c) international radio
    d) internet refollow

    Correct ans is:- a)infrared
    you gave: {q1}
    """)

    #Q2 for robotics
                    q2 = input("""2. What is the full meaning of PIR sensor?
    a) positive infrared
    b) point of infrared
    c) Passive infrared
    d) plus infrared 
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "c" or q2 == "passive infrared":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. What is the full meaning of PIR sensor?
    a) positive infrared
    b) point of infrared
    c) Passive infrared
    d) plus infrared 

    Correct ans is:- c)Passive infrared
    you gave: {q2}
    """)

    # Q3 for robotics
                    q3 = input("""3. What is the full meaning of RF?
    a) Radio frequency
    b) Radio free
    c) Radio fall
    d) Radio following
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "a" or q3 == "radio frequency":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. What is the full meaning of RF?
    a) Radio frequency
    b) Radio free
    c) Radio fall
    d) Radio following

    Correct ans is:- a)Radio frequency
    you gave: {q3}
    """)
    # Q4 for robotics
                    q4 = input("""4. What is the full meaning of AI?
    a) Artificial internet
    b) Artificial information
    c) Artificial interface
    d) Artificial intelligence
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "d" or q4 == "artificial intelligence":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. What is the full meaning of AI?
    a) Artificial internet
    b) Artificial information
    c) Artificial interface
    d) Artificial intelligence

    Correct ans is:- d)Artificial intelligence
    you gave: {q4}
    """)

    # Q5 for robotics
                    q5 = input("""5. what is the name of world best robot?
    a) Reco            
    b) Sophia
    c) Roba
    d) Seba
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "b" or q5 == "sophia":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. what is the name of world best robot?
    a) Reco            
    b) Sophia
    c) Roba
    d) Seba

    Correct ans is:- b)Sophia
    you gave: {q5}
    """)
            elif sub == "3" or sub == "math":
                    print("\n" + "="*47 + " Thank you for selected Math " + "="*47)
                    sleep_time()

    #Q1 for math
                    q1 = input("""1. Find the sum of 111 + 222 + 333
    a) 700
    b) 666
    c) 10
    d) 100
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "b" or q1 == "666":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. Find the sum of 111 + 222 + 333
    a) 700
    b) 666
    c) 10
    d) 100

    Correct ans is:- b)666
    you gave: {q1}
    """)

    #Q2 for math
                    q2 = input("""2. a = 10 & b = 5 then 2a+2b = ?
    a) 20
    b) 15
    c) 30
    d) 25
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "c" or q2 == "30":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. a = 10 & b = 5 then 2a+2b = ?
    a) 20
    b) 15
    c) 30
    d) 25

    Correct ans is:- c)30
    you gave: {q2}
    """)

    #Q3 for math
                    q3 = input("""3. a = 5 & b = 10 then (2a+2b)^2 = ?
    a) 400
    b) 150
    c) 300
    d) 900
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "d" or q3 == "900":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. a = 5 & b = 10 then (2a+2b)^2 = ?
    a) 400
    b) 150
    c) 300
    d) 900

    Correct ans is:- d)900
    you gave: {q3}
    """)

    #Q4 for math
                    q4 = input("""4. a = 5 & b = 10 then (2a-2b)^2 = ?
    a) 100
    b) 400
    c) 800
    d) 900
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "a" or q4 == "100":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. a = 5 & b = 10 then (2a-2b)^2 = ?
    a) 100
    b) 400
    c) 800
    d) 900

    Correct ans is:- a)100
    you gave: {q4}
    """)

    #Q5 for math
                    q5 = input("""5. a = 5 & b = 10 & c= 1 then (2a+2b+c)^2 = ?
    a) 100
    b) 300
    c) 49
    d) 900
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "d" or q5 == "900":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. a = 5 & b = 10 & c= 1 then (2a+2b+c)^2 = ?
    a) 100
    b) 300
    c) 49
    d) 900

    Correct ans is:- d)900
    you gave: {q5}
    """)
            elif sub == "4" or sub == "computer":
                    print("\n" + "="*47 + " Thank you for selected Computer " + "="*47)
                    sleep_time()

    #Q1 for computer
                    q1 = input("""1. When was the first computer invented?
    a) 1945
    b) 1943
    c) 1918
    d) 1937
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "b" or q1 == "1943":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. When was the first computer invented?
    a) 1945
    b) 1943
    c) 1918
    d) 1937

    Correct ans is:- b)1943
    you gave: {q1}
    """)


    #Q2 for computer
                    q2 = input("""2. What was the name of the first computer invented?
    a) ENIAC
    b) ENI
    c) ENCIA
    d) ENICA
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "a" or q2 == "eniac":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. What was the name of the first computer invented?
    a) ENIAC
    b) ENI
    c) ENCIA
    d) ENICA

    Correct ans is:- a)ENIAC
    you gave: {q2}
    """)

    #Q3 for computer
                    q3 = input("""3. Who is known as the father of computers?
    a) Pascal
    b) Hollerith
    c) Newman
    d) Charles Babbage
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "d" or q3 == "charles babbage":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. Who is known as the father of computers?
    a) Pascal
    b) Hollerith
    c) Newman
    d) Charles Babbage

    Correct ans is:- d)Charles Babbage
    you gave: {q3}
    """)

    #Q4 for computer
                    q4 = input("""4. When was the first 1 GB disk drive released in the world?
    a) 1980
    b) 1970
    c) 1981
    d) 1971
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "a" or q4 == "1980":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. When was the first 1 GB disk drive released in the world?
    a) 1980
    b) 1970
    c) 1981
    d) 1971

    Correct ans is:- a)1980
    you gave: {q4}
    """)

    #Q5 for computer
                    q5 = input("""5. What was the name of the first computer programmer?
    a) Alan Turing
    b) Ada Lovelace
    c) Tim Berners - Lee
    d) Steve Wozniak
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "b" or q5 == "ada lovelace":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. What was the name of the first computer programmer?
    a) Alan Turing
    b) Ada Lovelace
    c) Tim Berners - Lee
    d) Steve Wozniak

    Correct ans is:- b)Ada Lovelace
    you gave: {q5}
    """)
            elif sub == "5" or sub == "Sports":
                    print("\n" + "="*47 + " Thank you for selected Sports " + "="*47)
                    sleep_time()

    #Q1 for sports
                    q1 = input("""1. Who is hosting the 2026 World Cup?
    a) Canada
    b) Mexico
    c) United States
    d) All of the Above
    """).lower()
                    print(f"You selected = {q1}")

                    if q1 == "d" or q1 == "all of the above":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""1. Who is hosting the 2026 World Cup?
    a) Canada
    b) Mexico
    c) United States
    d) All of the Above

    Correct ans is:- d)All of the Above
    you gave: {q1}
    """)

    #Q2 for sports
                    q2 = input("""2. When was the first World Cup?
    a) 1926
    b) 1928
    c) 1930
    d) 1932
    """).lower()
                    print(f"You selected = {q2}")

                    if q2 == "c" or q2 == "1930":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""2. When was the first World Cup?
    a) 1926
    b) 1928
    c) 1930
    d) 1932

    Correct ans is:- c)1930
    you gave: {q2}
    """)

    #Q3 for sports
                    q3 = input("""3. What does PK mean?
    a) Pick'em
    b) Point Known
    c) Penalty Kick
    d) Personal Knowledge
    """).lower()
                    print(f"You selected = {q3}")

                    if q3 == "a" or q3 == "pick'em":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""3. What does PK mean?
    a) Pick'em
    b) Point Known
    c) Penalty Kick
    d) Personal Knowledge

    Correct ans is:- a)Pick'em
    you gave: {q3}
    """)

    #Q4 for sports
                    q4 = input("""4. Who has scored the most goals for the Brasil in World Cup history?
    a) Neymar
    b) Ronaldo
    c) Pele
    d) Zico
    """).lower()
                    print(f"You selected = {q4}")

                    if q4 == "c" or q4 == "pele":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""4. Who has scored the most goals for the Brasil in World Cup history?
    a) Neymar
    b) Ronaldo
    c) Pele
    d) Zico

    Correct ans is:- c)Pele
    you gave: {q4}
    """)

    #Q5 for sports
                    q5 = input("""5. Who is the richest player in the World Cup?
    a) Kylian Mbappe, France
    b) Cristiano Ronaldo, Portugal
    c) Neymar Jr., Brazil
    d) Lionel Messi, Argentina
    """).lower()
                    print(f"You selected = {q5}")

                    if q5 == "a" or q5 == "kylian mbappe, france":
                        ok +=1
                    else:
                        ng +=1
                        wrong.append(f"""5. Who is the richest player in the World Cup?
    a) Kylian Mbappe, France
    b) Cristiano Ronaldo, Portugal
    c) Neymar Jr., Brazil
    d) Lionel Messi, Argentina

    Correct ans is:- a)Kylian Mbappe, France
    you gave: {q5}
    """)
            else:
                    print("you are selected the wrong subject, please try again")
                    logging.info("user are selected wrong subject")

            if sub == "1" or sub == "2" or sub == "3" or sub == "4" or sub == "5":
                result_ok = int((ok/5)*100)
                result_ng = int((ng/5)*100)
                if result_ok == 100:
                    print ("\nCongratulations 😍")
                    print(f"you gave {result_ok} % correct answers")
                    logging.info(f"user gave {result_ok} % correct answers")
                elif result_ok > 50 and result_ok <100:
                    print ("\nCongratulations 🙂")
                    print(f"you gave {result_ok} % correct answers & {result_ng} % wrong answers")
                    logging.info(f"user gave {result_ok} % correct answers")
                    logging.info(f"user gave {result_ng} % wrong answers")
                else:
                    print("\n 😟😟😟")
                    print(f"you gave {result_ok} % correct answers & {result_ng} % wrong answers")
                    logging.info(f"user gave {result_ok} % correct answers")
                    logging.info(f"user gave {result_ng} % wrong answers")

                if len(wrong) != 0:

                    ask1 = input("are you want to see which question you gave the wrong answer to? ")
                    if ask1 != "yes":
                        logging.info("user aren't want to see worng answers")
                        pass
                    else:
                        logging.info("user want to see wrong answers")
                        for i in wrong:
                            print(i)
                            logging.info("%s",i)
                else:
                    print("🙂🙂🙂")

                    
except Exception as e:
    print(e)
    logging.error("Error is happend")
    logging.exception("error is %s",e) 
```


## You can follow me

Facebook:- https://www.facebook.com/problemsolvewithridoy/

Linkedin:- https://www.linkedin.com/in/ridoyhossain/

YouTube:- https://www.youtube.com/@problemsolvewithridoy

If you have any confusion, please feel free to contact me. Thank you


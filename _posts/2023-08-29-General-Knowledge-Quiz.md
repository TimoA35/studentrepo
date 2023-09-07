---
toc: flase
comments: false
layout: post
title: Timo's quiz
description:
type: hacks
courses: { csse: {week: 1}, csp: {week: 2, categories: [4.A]}, csa: {week: 0} }
categories: [C1.4]
---


### General Knowldge Quiz

import getpass, sys

def question_with_response(prompt):
    print("Question: " + prompt)
    msg = input()
    return msg

questions = 3
correct = 0

print('Hello, ' + getpass.getuser() + " running " + sys.executable)
print("You will be asked " + str(questions) + " questions.")
question_with_response("Are you ready to take a test?")

rsp = question_with_response("What command is used to include other functions that were previously developed?")
if rsp == "import":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")

rsp = question_with_response("What command is used to evaluate correct or incorrect response in this example?")
if rsp == "if":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")

rsp = question_with_response("Each 'if' command contains an '_________' to determine a true or false condition?")
if rsp == "expression":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")

print(getpass.getuser() + " you scored " + str(correct) +"/" + str(questions))

from random import choice

color_select_list = [0,1,2,3,4,5,6,7]

colors = {
    "white": 0,
    "red": 1,
    "green": 2,
    "blue": 3,
    "yellow": 4,
    "brown": 5,
    "orange": 6,
    "black": 7 
}

color_seq_list = {
    0: 0,
    1: 0,
    2: 0,
    3: 0
}


def pick_seq(num_colors):
    for x in range(num_colors):
        color_seq_list[x] = choice(color_select_list)
        color_select_list.remove(color_seq_list[x])

    # chosen colors
    # keylist = list(colors.keys())
    # print(keylist[int(color_seq_list[0])], keylist[int(color_seq_list[1])], keylist[int(color_seq_list[2])], keylist[int(color_seq_list[3])])



def guess(num_colors):
    correctness = 0
    user_input = input("Please enter the four colors in order :  ").split(',')

    for x in range(num_colors):
        placeholder = colors[user_input[x].strip()]
        if int(placeholder) == color_seq_list[x]:
            print('yep')
            correctness+=1
        elif int(placeholder) in color_seq_list.values():
            print('kinda')
        else:
            print('nop')

    return correctness


def play():
    turns = 5
    num_colors = len(color_seq_list)
    print(f"you have {turns} to win! Good Luck!")
    pick_seq(num_colors)

    for x in range(turns):
        correctness = guess(num_colors)
        if correctness == num_colors:
            print("you win!")
            break
        if x == turns-1:
            print("you lose!")

play()

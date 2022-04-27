# Alex Mudaliar
# W02 Prove: Developer - Solo Code Submission

# Variables
Current_Value = 1

# Gathers Names of the Players and Assigns the Values
Player_1_Name = input("Player 1 (X): Whats your name? ")
Player_2_Name = input("Player 2 (O): Whats your name? ")

# Start Print Statement
print()
print("Welcome to Tic-Tac-Toe")
print(f"{Player_1_Name} (X)")
print(f"{Player_1_Name} (O)")

# Creates Game Board
Board_Values = []
for i in range(9):
        Board_Values.append(i + 1)


# Function to print the board
def Print_Board(Board_Values):
    print()
    print(f"{Board_Values[0]} {Board_Values[1]} {Board_Values[2]}")
    print(f"{Board_Values[3]} {Board_Values[4]} {Board_Values[5]}")
    print(f"{Board_Values[6]} {Board_Values[7]} {Board_Values[8]}")

# Check the board for a winner
def Winner(board):
    return (board[0] == board[1] == board[2] or
            board[3] == board[4] == board[5] or
            board[6] == board[7] == board[8] or
            board[0] == board[3] == board[6] or
            board[1] == board[4] == board[7] or
            board[2] == board[5] == board[8] or
            board[0] == board[4] == board[8] or
            board[2] == board[4] == board[6])

# Check the board for a tie
def Draw(Board_Values):
    for value in range(9):
        if Board_Values[value] != "x" and Board_Values[value] != "o":
            return False
    return True 

# Determines the Current Player
def Current_Player(Current_Player_Value):
    if Current_Player_Value == 1:
        Current_Player_Value = 2
        return Current_Player_Value
    if Current_Player_Value == 2:
        Current_Player_Value = 1 
        return Current_Player_Value

# Determines the name of the Current Player
def Current_Players_Name(Current_Player_Value):
    if Current_Player_Value == 1:
        return Player_1_Name
    if Current_Player_Value == 2:
        return Player_2_Name

def Update_Game_Board(Game_Input, Board_Values, Current_Value):
    if Current_Value == 1:
        Board_Values[(Game_Input-1)] = "x"
        return Board_Values
    if Current_Value == 2:
        Board_Values[(Game_Input-1)] = "o"
        return Board_Values
    

# When Game is in Motion

while True:
    print()
    Current_Value = Current_Player(Current_Value)
    Print_Board(Board_Values)
    Name = Current_Players_Name(Current_Value)
    Player_Input = int(input(f"{Name}'s Turn, Choose a Position (1-9): "))
    Update_Game_Board(Player_Input, Board_Values, Current_Value)

    if Draw(Board_Values) == True:
        Print_Board(Board_Values)
        print()
        print("The game was a draw")
        break

    if Winner(Board_Values) == True:
        Print_Board(Board_Values)
        print()
        print(f"Congrats {Name} won the game")
        break

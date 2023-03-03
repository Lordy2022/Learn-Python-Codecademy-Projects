# Initial data.

letters = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
points = [1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 4, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10]

# 1) Using a list comprehension and zip, create a dictionary called letter_to_points that has the elements of letters as the keys and the elements of points as the values:

letters_to_points = {
  key: value
  for key, value in zip(letters, points)
}  

# 2) Our letters list did not take into account blank tiles. Add an element to the letter_to_points dictionary that has a key of " " and a point value of 0:

letters_to_points[" "] = 0

# 3) We want to create a function that will take in a word and return how many points that word is worth. Define a function called score_word that takes in a parameter word:

# 3.1) Inside score_word, create a variable called point_total and set it to 0:

# 3.2) After defining point_total, create a for loop that goes through the letters in word and adds the point value of each letter to point_total. You should get the point value from the letter_to_points dictionary. If the letter you are checking for is not in letter_to_points, add 0 to the point_total. After the loop is finished, return point_total:

def score_word(word):
  point_total = 0
  for letter in word:
    point_total += letters_to_points.get(letter, 0)
  return point_total

# 4) Let’s test this function! Create a variable called brownie_points and set it equal to the value returned by the score_word() function with an input of "BROWNIE":

brownie_points = score_word("BROWNIE")

# 5) We expect the word BROWNIE to earn 15 points, let’s print out brownie_points to make sure we got it right:

print(brownie_points)

# 6) Create a dictionary called player_to_words that maps players to a list of the words they have played. This table represents the data to transcribe into your dictionary:

player_to_words = {
  "Player 1": ["BLUE", "TENNIS", "EXIT"],
  "Player 2": ["EARTH", "EYES", "MACHINE"],
  "Player 3": ["ERASER", "BELLY", "HUSKY"],
  "Player 4": ["ZAP", "COMA", "PERIOD"],
}

# 7) Create an empty dictionary called player_to_points:

# 7.1) Iterate through the items in player_to_words. Call each player player and each list of words words. Within your loop, create a variable called player_points and set it to 0:

# 7.2) Within the loop, create another loop that goes through each word in words and adds the value of score_word() with word as an input:

# 7.3) After the inner loop ends, set the current player value to be a key of player_to_points, with a value of player_points:

player_to_points = {}
for player, words in player_to_words.items():
  player_points = 0
  for word in words:
    player_points += score_word(word)
  player_to_points[player] = player_points

# 8) player_to_points should now contain the mapping of players to how many points they’ve scored. Print this out to see the current standings for this game! If you’ve calculated correctly, 'Player 2' should be winning by 1 point:

print(player_to_points)

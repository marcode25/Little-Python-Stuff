import random

def get_user_numbers():
	print("Please select 3 numbers bewteen 1 and 10")
	numbers = []
	while len(numbers) < 3:
		try:
			num = int(input(f"Number {len(numbers) + 1}: "))
			if 1 <= num <= 10:
				numbers.append(num)
			else:
				print("please enter a valid number between 1 and 10")
		except ValueError:
			print("Please enter a valid number.")
	return numbers


def play_lottery():
	winning_numbers = random.sample(range(1, 11), 3)
	user_numbers = get_user_numbers()
	print("Your numbers: ", user_numbers)
	print("Winning numbers: ", winning_numbers)

	matches = set(user_numbers) & set(winning_numbers)

	print("You matched: ", len(matches), " number(s): ", sorted(matches))

	if len(matches) == 3:
		print("Congrats you won 1000 dollars!!")
	else:
		print("too bad you lost")
	
def main():
	print("Welcome to the lottery game")
	while True:
		play_lottery()
		play_again = input("You want to play again y/n ").lower()
		if play_again != "y":
			print("Thanks for playing")
			break
main()

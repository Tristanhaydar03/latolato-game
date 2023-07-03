# Lato-Lato Game

import random

choices = ['batu', 'gunting', 'kertas']

def play_game():
    print("Selamat datang di permainan Lato-Lato!")
    print("Pilih: 1 - Batu, 2 - Gunting, 3 - Kertas")

    while True:
        player_choice = input("Masukkan pilihanmu (1/2/3): ")
        
        if player_choice in ['1', '2', '3']:
            player_choice = int(player_choice) - 1
            break
        else:
            print("Pilihan tidak valid. Silakan pilih lagi.")

    computer_choice = random.randint(0, 2)

    print("Pilihanmu: " + choices[player_choice])
    print("Pilihan Komputer: " + choices[computer_choice])

    if player_choice == computer_choice:
        print("Hasil: Seri!")
    elif (player_choice == 0 and computer_choice == 1) or \
         (player_choice == 1 and computer_choice == 2) or \
         (player_choice == 2 and computer_choice == 0):
        print("Hasil: Kamu menang!")
    else:
        print("Hasil: Komputer menang!")

play_game()

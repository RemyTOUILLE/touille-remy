# Mon Blog Python
import random
import time
import os

# Fonction pour effacer l'écran (fonctionne sur Windows, MacOS et Linux)
def clear_screen():
    os.system('cls' if os.name == 'nt' else 'clear')

# Couleurs pour le terminal
class Colors:
    BLUE = '\033[94m'
    GREEN = '\033[92m'
    YELLOW = '\033[93m'
    RED = '\033[91m'
    PURPLE = '\033[95m'
    CYAN = '\033[96m'
    END = '\033[0m'
    BOLD = '\033[1m'

# Liste de citations sur la programmation
quotes = [
    "Le code, c'est comme l'humour. Quand on doit l'expliquer, c'est mauvais.",
    "Il y a deux façons d'écrire des programmes sans bugs. Seule la troisième fonctionne.",
    "Un bon développeur est celui qui cherche la simplicité avant la complexité.",
    "La programmation n'est pas à propos des ordinateurs, mais à propos des personnes.",
    "Programmeur: un organisme qui transforme le café en code.",
    "Le meilleur débugger au monde est un bon night de sommeil.",
    "Python est le seul langage qui est à la fois un serpent et pas un serpent.",
    "Tout le monde sait qu'un bon développeur Python n'utilise pas de parenthèses.",
    "La vie est trop courte pour écrire du code sans indentation.",
    "Les bons programmeurs écrivent du code que les humains peuvent comprendre.",
    "Le code est comme une blague. S'il a besoin de commentaires, il n'est pas bon.",
    "Si le débogage est l'art de retirer les bugs, alors la programmation doit être l'art de les créer.",
    "Le premier 90% du code représente les premiers 90% du temps de développement. Les 10% restants représentent les autres 90% du temps de développement.",
    "Une IA écrit du code? Intéressant. Mais qui va écrire les commentaires sarcastiques?"
]

# Fonction principale
def quote_generator():
    while True:
        clear_screen()
        print(f"\n{Colors.BOLD}{Colors.YELLOW}=== GÉNÉRATEUR DE CITATIONS PYTHON ==={Colors.END}\n")
        
        # Choix aléatoire d'une citation et d'une couleur
        quote = random.choice(quotes)
        color_choice = random.choice([Colors.BLUE, Colors.GREEN, Colors.RED, Colors.PURPLE, Colors.CYAN])
        
        # Afficher la citation avec un effet de machine à écrire
        print(f"{color_choice}❝", end="")
        for char in quote:
            print(char, end='', flush=True)
            time.sleep(0.03)
        print(f"❞{Colors.END}\n")
        
        # Options pour l'utilisateur
        print(f"{Colors.BOLD}Options:{Colors.END}")
        print("1. Nouvelle citation")
        print("2. Ajouter une citation")
        print("3. Quitter")
        
        choice = input("\nEntrez votre choix (1-3): ")
        
        if choice == '1':
            continue
        elif choice == '2':
            new_quote = input("\nEntrez votre nouvelle citation: ")
            if new_quote:
                quotes.append(new_quote)
                print(f"{Colors.GREEN}Citation ajoutée avec succès!{Colors.END}")
                time.sleep(1.5)
        elif choice == '3':
            clear_screen()
            print(f"\n{Colors.YELLOW}Merci d'avoir utilisé le générateur de citations Python!{Colors.END}")
            print(f"{Colors.CYAN}À bientôt sur le blog Python!{Colors.END}\n")
            break
        else:
            print(f"{Colors.RED}Choix non valide. Veuillez réessayer.{Colors.END}")
            time.sleep(1.5)

# Lancer le programme
if __name__ == "__main__":
    quote_generator()
Bienvenue sur mon blog d'apprentissage Python!

## Articles récents
- Mon parcours d'apprentissage
- Installation de Python

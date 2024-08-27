#include <iostream>
#include <filesystem>
#include <string>
#include <vector>

namespace fs = std::filesystem;

// Function declarations
void displayMainMenu();
void listFilesMenu();
void createDirectory();
void changeDirectory();
void listAllFiles();
void listFilesByExtension();
void listFilesByPattern();

int main() {
    while (true) {
        displayMainMenu();
        int choice;
        std::cin >> choice;

        switch (choice) {
            case 1:
                listFilesMenu();
                break;
            case 2:
                createDirectory();
                break;
            case 3:
                changeDirectory();
                break;
            case 4:
                std::cout << "Exiting the program." << std::endl;
                return 0;
            default:
                std::cout << "Invalid choice. Please try again." << std::endl;
        }
    }
}

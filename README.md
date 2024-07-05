# Fast Reader

Reader is a versatile application designed to assist users in reading text swiftly and effectively. Developed using the GTK library in C++, this program offers a customizable interface to enhance the reading experience.

**Version 4 image**:

![Bildschirmfoto vom 2024-07-05 21-01-55](https://github.com/Quantum-mutnauQ/Fast-Reader-GTK/assets/141065355/48d57ddf-fe5d-4209-aaed-1b30403e1816) ![Bildschirmfoto vom 2024-07-05 21-08-48](https://github.com/Quantum-mutnauQ/Fast-Reader-GTK/assets/141065355/cc7e675b-7642-43a6-a2a9-a5eecfc2e72d)

## Features

- **Customizable Settings**: Tailor your reading experience by adjusting settings like background color, text color, font size, and display of progress indicators.
- **Text Input**: Easily input text into the application through a dedicated text entry field.
- **Word-by-Word Display**: The text is broken down into individual words, presented one at a time, facilitating focused reading.
- **Navigation Options**: Seamlessly navigate through the text using intuitive navigation buttons or convenient keyboard shortcuts.
- **Progress Indicators**: Keep track of your reading progress with helpful indicators displaying your current position in the text and overall progress.
- **Time-Based Word predictions**: You can set a variable time calculate by a formal for the display of each word. The formula for calculating the word display time is: "Time-Per-Word × (Cube Root of Word-Length)". This dynamic adjustment ensures that longer, more complex words are allotted more time, providing a natural and responsive reading experience.

 You can set a variable time limit for the display of each word. The formula for calculating the word display time is: "Time-Per-Word × (Cube Root of Word-Length)" (Time−Per−Word×(₃√Word−Length )). This dynamic adjustment ensures that longer, more complex words are allotted more time, providing a natural and responsive reading experience.
  
## Getting Started

To begin using Fast Reader, follow these simple steps:

1. **Installation**: Download the latest release and extract the contents from the zip file.
2. **Execution**: Run the compiled "SpeedReader" executable. You can execute it by running `./FastReader` in the folder where the program is saved, or simply double-click on it.
3. **Troubleshooting** You need to install `libgtk-4-1` and `libconfig9`.

## Adding a New Language

1. **Create Files**: Within the "locales" folder, create a subfolder named with the short of your language. Inside this folder, create another folder named `LC_MESSAGES`. Then, within this folder, create a file named `FastReader.po`.
2. **Add Translations to File**: Copy the provided template and modify the English phrases to their equivalents in your language in the speedreader.po file.
```
msgid ""
msgstr ""
"Content-Type: text/plain; charset=UTF-8\n"

msgid "Error while writing file.\n"
msgstr "Error while writing file.\n"

msgid "Error while reading file: %s:%d - %s\n"
msgstr "Error while reading file: %s:%d - %s\n"

msgid "Trye to corrct"
msgstr "Try to correct"

msgid "Einstellungen:"
msgstr "Settings:"

msgid "Hintergrund:"
msgstr "Background:"

msgid "Schrift:"
msgstr "Font:"

msgid "Schrift Größe:"
msgstr "Font Size:"

msgid "Fortschritt Zeigen:"
msgstr "Show Progress:"

msgid "Angezeigte wörter:"
msgstr "Displayed Words:"

msgid "Zeitbassirt nechstes Wort:"
msgstr "Time-based Next Word:"

msgid "Zeit (sec):"
msgstr "Time (sec):"

msgid ""
"Die Zeit wird berechnet durch:\n"
"Zeit−Pro−Wort×(₃√Wort−Länge )"
msgstr ""
"The time is calculated by:\n"
"Time−Per−Word×(₃√Word−Length )"

msgid "Zurücksetzen"
msgstr "Reset"

msgid "Lesen"
msgstr "Read"

msgid "Zurück"
msgstr "Back"

msgid "Konnte das Standard-Konfigurationsverzeichnis nicht abrufen.\n"
msgstr "Could not retrieve the default configuration directory.\n"

msgid "Fehler beim Erstellen des Verzeichnisses FastReader.\n"
msgstr "Error creating the FastReader directory.\n"

msgid "Fast Reader"
msgstr "Fast Reader"
 ```
3. **Compile**: Use the `msgfmt` command to compile the language file. For example: `msgfmt locale/<YourLanguage>/LC_MESSAGES/FastReader.po -o locale/<YourLanguage>/LC_MESSAGES/FastReader.mo`.
4. **Testing**: Launch Fast Reader and verify that the new language is working correctly. If any issues arise, please open an issue and provide your `FastReader.po` file and language details.
5. **Support the Project (Optional)**: Open an issue and share your `FastReader.po` file along with your language details, and we will add it to the project.

## Compiling It Yourself

1. **Download the Code**: Download the latest code.
2. **Compilation**: Compile it using the following command:
3. ```g++ -std=c++11  -o FastReader FastReader.cpp `pkg-config --cflags --libs gtk4 libconfig` && msgfmt locale/de/LC_MESSAGES/FastReader.po -o locale/de/LC_MESSAGES/FastReader.mo && msgfmt locale/en/LC_MESSAGES/FastReader.po -o locale/en/LC_MESSAGES/FastReader.mo```. If any issues arise, ensure you have `GCC`, `msgfmt`, `libconfig-dev`,and `libgtk-4-dev` installed.

## Plans for the future 
1. Include statistics like time per word. (Version 5)

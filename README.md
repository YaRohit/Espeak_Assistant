# Espeak_Assistant
# C++ Text-to-Speech Personal Assistant

- C++ text to speech application which acts as a personal assistant.

Firstly one must download and install espeak speech synthesizer. The link is:http://espeak.sourceforge.net/download.html Now the espeak.exe application must be placed in the same folder where the c++ application is being stored.

## Prerequisites

Before running the application, you need to download and install the eSpeak speech synthesizer. You can download it from the following link: [eSpeak Download](http://espeak.sourceforge.net/download.html). Place the `espeak.exe` application in the same folder where the C++ application is stored.

## Usage

The application provides two main functionalities:

1. Text-to-Speech Conversion: To listen to the speech

Replace `whatever message you want to listen to` with the message you want the application to speak out loud. Run the application to listen to the speech.

2. System Commands: The application can also execute various system commands.


## Note

- Replace the placeholders with the appropriate file paths and messages in the provided code examples.
- To use the text-to-speech functionality, run the application and listen to the spoken message.
- Use the system commands to open files, launch applications, and play audio as per your requirements.

If you need to listen to the speech, then you must include these 4 lines of code:

string phrase = "whatever message you want to listen to"; string command = "espeak "" + phrase + """; const char *charCommand = command.c_str(); system(charCommand);

To open any file format in the system, then command is: ShellExecute(NULL,"open","file path",NULL, NULL, SW_NORMAL);

Note: in file path, please put two \ wherever there is one \

To open a browser: system("start url of browser"); Example: system("start https://www.youtube.com");

To open .exe files such as ms word,paint,excel notepad etc: CreateProcess(TEXT("file path"), NULL, NULL, NULL, FALSE, NULL, NULL, NULL, &startInfo, &processInfo);

To play audio using mcisendstring: mciSendString("open "path of audio" type mpegvideo alias mp3", NULL, 0, NULL); mciSendString("play mp3", NULL, 0, NULL);

Feel free to customize the application to add more features or enhance its functionality according to your needs.


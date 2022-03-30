# Import-.py-file-with-pyqt6-interface
How to import a .py file converted from a .ui to a .py project

I was with a problem to import a .py file to a new .py file, because when we import a .ui file, we need to search for the functions before to use on the file, and it is too bad to make our programs.

To solution the problem I always transform the .ui file to a .py file and them make my modifications, but when I need to add or moddify anything in the interface I need to transform the .ui file again and adapt the converted file to my actual file.

But transform the .ui file to a .py file and them import to my project is the solution, because I can use all the functions, labels, widgets and etc from my transformed file without to search for every one to use, and when I need to change anything in the interface I only need to transform the .ui file to the same .py file and preserve all of my code.

How to do.

Create a .ui file
![image](https://user-images.githubusercontent.com/73801806/160836067-b6e8c89c-6330-4766-80b8-a0987ff95391.png)

Save the file and convert with the command "pyuic6 -x input.ui -o output.py"
![image](https://user-images.githubusercontent.com/73801806/160836770-b0b1ef12-d45b-4fdc-89c9-c0b4860b5a92.png)

Open the output.py file and copy the "if __name__ == "__main__":" section and the imports to another .py file.
![image](https://user-images.githubusercontent.com/73801806/160837492-53b07592-82d5-4dde-aa93-4c2362633fbe.png)
![image](https://user-images.githubusercontent.com/73801806/160837542-3ac471e3-ced3-4fd7-bfc4-44867de9ae64.png)

Add the import "import output as interface"
![image](https://user-images.githubusercontent.com/73801806/160837887-6a225bd9-3ec7-47c0-8b32-bca58a024388.png)

After import, just change the ui = Ui_MainWindow() adding the interface. before
![image](https://user-images.githubusercontent.com/73801806/160838175-edefe57d-c33d-4439-b5c9-afa2b226e2f5.png)

Now the interface works from this file, and to modify the interface, create a class and a def method and call in the if __name__ == "__main__":, and inside the def call the Ui_MainWindow and the setupUi from the imported file to modidy.

![image](https://user-images.githubusercontent.com/73801806/160840247-5e6b172b-cf78-4079-a1e9-9de5a85c0c11.png)


[gitInterface.zip](https://github.com/maycon2-0/Import-.py-file-with-pyqt6-interface/files/8380660/gitInterface.zip)

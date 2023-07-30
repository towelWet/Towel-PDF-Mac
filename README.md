Sure, here are the steps to create an application bundle with Platypus:

1. **Open Platypus**: Launch the Platypus application.

2. **Create a new script**: Click on the "+New" button at the bottom left of the Platypus window.

3. **Set the script type**: In the "Script Type" dropdown menu, select "Shell".

4. **Set the interface type**: In the "Interface" dropdown menu, select "None".

5. **Add your scripts and files**: Click on the "Bundled Files" tab, then click on the "+" button at the bottom. In the file dialog that opens, navigate to the `env` directory and the `towel-pdf.py` script, select them, and click "Open". These files will be bundled into the .app file.

6. **Create the shell script**: Click on the "Script" tab, then enter the following script in the text area:

```bash
#!/bin/bash
export PYTHONPATH=./env/bin/python3
./env/bin/python3 towel-pdf.py
```

This script sets the `HOME` environment variable, changes the current directory to the directory where the script is located, and then runs the `towel-pdf.py` script using the Python interpreter from the virtual environment.

7. **Set the app settings**: Click on the "App Settings" tab, then enter the following settings:

- **App Name**: Enter the name of your app, such as "Run Towel Pdf".
- **App Icon**: If you have an icon for your app, click on the "Set Icon..." button, navigate to the icon file in the file dialog that opens, select it, and click "Open".
- **Identifier**: Enter a unique identifier for your app, such as "org.traope.RunTowelPdf".
- **Author**: Enter your name.
- **Version**: Enter the version of your app, such as "1.0".

8. **Create the .app file**: Click on the "Create App" button at the bottom right of the Platypus window. In the file dialog that opens, navigate to the directory where you want to save the .app file, enter a name for the .app file, and click "Save".

After following these steps, you should have a .app file that runs your Python script when launched. If you encounter any issues, please provide more details about the issue, such as any error messages you're seeing.

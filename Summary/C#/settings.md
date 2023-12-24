# Settings

## Check to see if .NET is already installed

1. Open the Windows Command Prompt

1. At the command prompt, type: `dotnet --version` and then press the Enter key.

1. If a version of .NET is installed, you should see a response message listing the version number similar to the following: `8.0.100`

1. If the .NET 8 Software Development Kit isn't already installed, [install it](https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/3-exercise-install-dotnet) now.

## Create a C# console application in a specified folder

1. At the Terminal command prompt, to create a new console application in a specified folder, enter the following command:

    ```
    dotnet new console -o ./CsharpProjects/TestProject
    ```


    This .NET CLI command uses a .NET program template to create a new C# console application project in the specified folder location. The command creates the CsharpProjects and TestProject folders for you, and uses TestProject as the name of your `.csproj` file.  


1. In the EXPLORER panel, expand the CsharpProjects folder.

    You should see the TestProject folder and two files, a C# program file named `Program.cs` and a C# project file named `TestProject.csproj`. The CLI command uses the folder name when it creates the project file (`TestProject.csproj`). The `Program.cs` file is the file containing your C# code.

1. In the EXPLORER panel, to view the C# code in the Editor panel, select `Program.cs`.

    As you can see, the default console application is the iconic “Hello World!” application.

    ```C#
    // See https://aka.ms/new-console-template for more information
    Console.WriteLine("Hello, World!");
    ```

    
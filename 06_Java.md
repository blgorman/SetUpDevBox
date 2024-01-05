# Install Java and validate that it is working

In this walkthrough you'll get Java installed on your machine and validate that it is working.

>**Note:** This is optional and should only be done if you are going to be developing in Java on your machine.  If you are only doing .NET development, you should skip this step.

## Task 1 - Install Java

To get Java installed on your machine, you'll need to download the latest SDK and install it.

1. Download Java

    [Java Downloads](https://www.oracle.com/java/technologies/downloads/#jdk21-windows)  

1. Download the MSI for x64  (or x86 if you have a 32-bit machine).
1. Run the MSI to install Java
1. Ensure Java is installed by running the following commands from the command line:

    ```bash
    javac -version
    java -version
    ```
1. If your computer doesn't recognize the `javac` or `java` commands, you'll need to add the Java bin directory to your path.  You can do this by following the instructions here:

    [Add Java to Path](https://www.java.com/en/download/help/path.xml)

## Task 2 - Validate Java is installed

Once you have Java installed and working, create a simple program in VSCode to validate that it is working.

1. Get VSCode Java extensions
1. Create a simple Java program

    ```java
    public class helloWorld {
        public static void main(String[] args) {
            System.out.println("Hello World! I am awesome!");
        }
    }
    ```
1. Run the program

    ```bash
    javac helloWorld.java
    java helloWorld
    ```  

1. Validate the output

    Ensure you see the following output:  
    ```bash
    Hello World! I am awesome!
    ```

1. Run and Debug with VSCode tools

    You can also run and debug the program using the VSCode tools.  This is beyond the scope of this walkthrough, but you can find instructions here:

    [Java in VSCode](https://code.visualstudio.com/docs/languages/java)

## Conclusion

At this point you should have Java working on your machine.  If you are going to be doing production-level Java development, you should also install Eclipse, Netbeans, or IntelliJ.  For academic Java development, VSCode should be sufficient.  Additionally, if you need more help, look into a simple Java IDE like BlueJ.

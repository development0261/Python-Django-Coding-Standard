# Coding Standard
Improve Your Coding Standard Through the following guidlines.
1. We run our hooks on every commit to automatically point out issues in code such as missing semicolons, trailing whitespace, and debug statements.
   * pip install pre-commit
#

2. Use single quotes for strings, or a double quote if the string contains a single quote. Don’t waste time doing unrelated refactoring of existing code to conform to this style.
#

3. Here indentation of arguments makes them grouped, and stand clear from others.
  ``` 
  def some_function_name(
       var_first, var_second, var_third,
       var_fourth):
   print(var_first)
   ```
#

4. extra indentation is not required, if you want to use extra indentation to ensure that the code will work, you can use the following coding style:
    ```
    if (this
       and that):
       do_something()
    ```
#

5. Black can reformat your entire file in place according to the Black code style. It helps your brain focus on the problem you want to solve and code solutions, rather than getting distracted by code structure and minor stylistic differences.
      * Black can be installed by running pip install black.
      * Note that Black defaults to 88 characters for its line length, but you can change that using the “-l” or “- -line-length” option.

          * For example, to change to 60 characters: black -l 60 python_file.py .
 #
 
 6. Every programming language and framework has its own naming convention. The naming convention in Python/Django is more or less the same, but it is worth mentioning it here. You will need to follow this while creating a variable name or global variable name and when naming a class, package, modules, and so on.
      * Name the variables properly: Never use single characters, for example, ‘x’ or ‘X’ as variable names. It might be okay for your normal Python scripts, but when you are building a web application, you must name the variable properly as it determines the readability of the whole project.
      * Naming of packages and modules: Lowercase and short names are recommended for modules. Underscores can be used if their use would improve readability. Python packages should also have short, all-lowercase names, although the use of underscores is discouraged.
      * Since module names are mapped to file names (models.py, urls.py, and so on), it is important that module names be chosen to be fairly short as some file systems are case insensitive and truncate long names.
      * Naming a class: Class names should follow the CamelCase naming convention, and classes for internal use can have a leading underscore in their name.
      * Global variable names: First of all, you should avoid using global variables, but if you need to use them, prevention of global variables from getting exported can be done via __all__, or by defining them with a prefixed underscore (the old, conventional way).
      * Function names and method argument: Names of functions should be in lowercase and separated by an underscore and self as the first argument to instantiate methods. For classes or methods, use CLS or the objects for initialization.
      * Method names and instance variables: Use the function naming rules—lowercase with words separated by underscores as necessary to improve readability. Use one leading underscore only for non-public methods and instance variables.

# Why Choose Object Oriented Programming in Python?
1. Python was designed with OOP approach and it offers the following advantages:
    * Provides a clear program structure and a clean code
    * Facilitates easy maintenance and modification of existing code
    * Since the class is sharable, the code can be reused
    * Since the class is sharable, the code can be reused and many other such Advantages.

# The Code layout:
  * Imports, Blank Lines, and the Indentations:
    The import should be in a particular sequence. At first, the standard libraries, then the third party, and at the last, the local libraries should be imported. If you only     need a single function/class from the import, do an absolute import. It makes your code much cleaner, accurate, and easy to identify. Don’t forget to add a space between     different types of imports.

  * There should be two blank lines surrounding classes and top-level functions. The methods inside of the class should be surrounded by a single blank line only. The preferred method of indentation is spaces, the 4 spaces indentation is accepted and accurate, but still, most people prefer tab indentation. Please keep in mind not to mix both spaces and tabs for indentation.
         

      * Don't forget to add a space between different group of imports

      * first of all, the standard library imports
       ```
        import standard_library_import_a
        import standard_library_import_b
        
       ```
        
      * then,the third party imports
        ```
        import third_party_import_a
        import third_party_import_b
        import third_party_import_c
        ```
      * at the last, local library import

        ```
        from local_library import local_a, local_b
        from local_library_two import local_c
        ```

      * two blank lines for top level functions

        ```
        def top_level_function(argument):
        ```
      * A standard four space indent
        ```
        print(argument)
        ```
   * Whitespaces, Trailing Commas, and String Quotes
      * One should avoid extra white spaces, there must be a single white space around both sides of an operator, one after the comma and none inside opening or closing of       parenthesis. Both single quotes and double quotes are acceptable in python, you should use both if you need quotes inside quotes to avoid syntax error and extra backslash.
        * Examples of commas and whitespaces
          ```
              x,  y = 30,  "text inside quotes"
              z = 'text inside quotes'
              if x == 30: print(x, y, z)
          ```
        * how to use quotes inside quotes
        ```
              text = "This text is using 'the single quote' inside double quote"
              print(text)
        ```
   * Naming Conventions
      * Use grammatically correct variable names, the class name should start with an uppercase and must follow camelCase convention If more than two words are to be used. In the same way, a function name should be joined with an underscore, and it must be lowercase. In method arguments, always use self as the first argument to declare an instance variable. In the same way, use ‘cls’ for the first argument for the class method. If the function name clashes with a reserved argument, use an underscore instead of a wrong spelling. Constants are declared in all capital letters.
          * class name follows camelcase convention
          ```
            class StudentDetails:

            def __init__(self, first_name, last_name):
            self.first_name = first_name
            self.last_name = last_name
          ```
          * Method name, variable names in lowercase joined with an underscore
          ```
            def grade(self, marks_obtained):
          ```
          * constants in capital
          ```
            GRACE = 2
            marks_obtained = GRACE + marks_obtained
            if marks_obtained > 90:
            self.student_grade = 'A'
            elif marks_obtained > 70:
            student_grade = 'B'
            else:
            student_grade = 'C'
          ```

   * Exception Handling for every critical situation
        ```
            try:
            file = open('filename.txt')
            file.write('Hello World')

            except Exception as e:
            print('Cannot open the file :', e)

            finally:
            file.close()
        ```
   
   * Use DRY (Don’t Repeat Yourself):
      * Always use the DRY principle to reuse the code. The best way to do it is to use functions and classes. The common functions can be put into a separate utils.py file and can be used several times instead of creating similar functions again and again.
Suppose if you need to read three files, instead of writing code for file read thrice, you can read it as a function and save your time.
          * function to read the file read
          ```
          def file_read(filename):
          with open(filename, 'r') as f:
          return f.read()

          qualities = file_read('quality.txt')
          description = file_read('description.txt')
          summary = file_read('summary.txt')
          ```
   * What to use? Tuples, Lists of Dictionaries
      * Use tuples when data is non-changeable, dictionaries when you need to map things, and lists if your data can change later on.
        
          * tuples are used when data is constant
            ```
            colors_of_rainbow = ('V', 'I', 'B', 'G', 'Y', 'O', 'R')
            ```
          * lists where data can be mutated
             ```
            movies_to_watch  = ['Inception', 'Iron Man', 'Wonder Woman']
            ```
          * Using lists in mapping is wrong
          * O(n) time would be taken to extract marks
            ```
            marks_obtained = [['History', 30], ['English', 35], ['Physics', 45]]
            ```
          * dicts when mapping is needed
          * dicts take O(1) time to get key value
            ```
            marks_obtained = {'History': 30, 'English': 35, 'Physics': 45}
            ```

   * Use the ‘with’ statement while opening a file, the ‘with’ statement closes the file even if there is an exception raised
      ```
        import csv
        with open('filename.csv', 'r') as file:
        csv_reader = csv.reader(file)
        for line in csv_reader:
        print(line)
      ```
  

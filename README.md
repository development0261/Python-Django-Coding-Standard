# Coding Standard
Improve Your Coding Standard Through following the guidlines.
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



### IO
* get path of current running program
~~~ C#
  dynamic type = (new Program()).GetType();
  string currentDirectory = Path.GetDirectoryName(type.Assembly.Location);
  Console.WriteLine(currentDirectory);
~~~

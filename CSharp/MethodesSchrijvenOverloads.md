# Overloads van zelf geschreven methods

Deze class heeft 2 **overloads** van de method `Groet` :

- `void Groet()` zonder parameter
- `void Groet(string naam)` met een string als parameter

```
class Program {

  static void Groet() {
    Console.WriteLine("Hallo!");
  }
  
  static void Groet(string naam) {
    Console.WriteLine("Hallo {0}!", naam);
  }

  static void Main() {
    Groet();
    Groet("Jos");
    Groet("Jan");
  }

}
```


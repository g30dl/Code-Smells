<h1><strong>Inappropriate Intimacy</strong></h1>
One class uses the internal fields and methods of another class. 

 Example:
```java
class Box {
    public int length;
    public int width; 
    public int height;

    Box() {
      this.length = 1;
      this.width = 1;
      this.height = 1;
    }
    
    public int getArea() {
      return 2 * (this.height * this.width) + 2 * (this.height * this.length) + 2 * (this.length * this.width);
    }
}

public class ShapeCalculator {
    Box box;
    
    ShapeCalculator() {
        this.box = new Box();
      }
      
    public int getBoxArea() {
        return this.box.getArea();
      }
      
    public int getBoxVolume() {
        return this.box.length * this.box.width * this.box.height;
      }
}
```
The "inappropriate intimacy" code smell is violated because the <strong>ShapeCalculator</strong> class directly accesses the public attributes of the <strong>Box</strong> class (length, width, height), exposing internal details of Box that should be encapsulated. Instead of interacting with Box through methods that abstract its implementation, ShapeCalculator relies on the internal structure of Box, increasing coupling and reducing the flexibility of the system.
  
adapted from:  https://github.com/alpgokcek/js-code-smells/blob/master/InappropriateIntimacy.md 

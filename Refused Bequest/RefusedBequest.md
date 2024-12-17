<h1><strong>Refused Bequest</strong></h1>

Someone was motivated to create inheritance between classes only by the desire to reuse the code in a superclass. But the superclass and subclass are completely different.



Example
```java
public abstract class Unit {
        public abstract void attack();
        public abstract void move();
}

public class Soldier extends Unit{
        @Override
        public void attack() {
        // Execute melee attack 
}
        @Override
        public void move() {
        // Execute movement logic
}

public class Tower extends Unit {
    @Override
    public void attack() {
        // Execute ranged attack
    }
    @Override
    public void move() {
        throw new UnsupportedOperationException("Move is not supported for Tower");
    }
}
```
Adapted from: https://luzkan.github.io/smells/refused-bequest

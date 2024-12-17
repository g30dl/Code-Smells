Refused Bequest

Someone was motivated to create inheritance between classes only by the desire to reuse the code in a superclass. But the superclass and subclass are completely different.



Example

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

Adapted from: https://luzkan.github.io/smells/refused-bequest

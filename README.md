### Task 8 kyu

[Task link](https://www.codewars.com/kata/5ab6538b379d20ad880000ab)

You are given the length and width of a 4-sided polygon. The polygon can either be a rectangle or a square.
If it is a square, return its area. If it is a rectangle, return its perimeter.

### My solution

```Java

public class Solution {
    public static int areaOrPerimeter (int l, int w) {
        if (l==w){return l*l;}
        else {return 2*(l+w);}
    }
}

```

### Favourite solution from code-wars

```Java

public class Solution {

    public static int areaOrPerimeter (int l, int w) {
        PolygonFactory factory = new PolygonFactory();
        Polygon polygon = factory.polygonFrom(w, l);
        return polygon.measure();
    }
}

class PolygonFactory {

    Polygon polygonFrom(int w, int l) {
        return w == l ? new Square(w, l) : new Rectangle(w, l);
    }

}

interface Polygon {

    int measure();
}

class Rectangle implements Polygon {
    private final int l;
    private final int w;

    Rectangle(int l, int w) {
        this.l = l;
        this.w = w;
    }

    public int measure() {
        return 2 * (l + w);
    }

}

class Square implements Polygon {
    private final int l;
    private final int w;

    Square(int l, int w) {
        this.l = l;
        this.w = w;
    }

    public int measure() {
        return w * w;
    }

}

```

I m looking at this solution and I have flashbacks from previous year of studying, haha

# Have a nice day!
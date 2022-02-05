# Triangle

```Triangle.java
package Triangle;

public class Triangle {
	public String check (int a, int b, int c) {
		if (a <= 200 && a >= 1 && b <= 200 && b >= 1 && c <= 200 && c >= 1) {
			if ((a + b) > c && (b + c) > a && (c + a) > b) {
				if (a == b && b == c) {
					return "Equilateral";
				} else if (a == b || b == c || c == a) {
					return "Isosceles";
				}
				return "Scalene";
			}
			return "Invalid";
		}
		return "Invalid";
	}
}
```

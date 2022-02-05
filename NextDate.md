# Next Date

```NextDate.java
package NextDate;

public class NextDate {
	
	public String findNext(int d, int m, int y, int number_of_days) {
		if (d == number_of_days) {
			d = 1;
			if (m == 12) {
				m = 1;
				y ++;
			} else {
				m ++;
			}
		} else if (d < number_of_days) {
			d ++;
		} else {
			return "Invalid Date";
		}
		return ""+d+"-"+m+"-"+y;
	}
	
	public String check(int d, int m, int y) {
		if (d >= 1 && d <= 31 && m >= 1 && m <= 12 && y >= 1812 && y <= 2012) {
			switch (m) {
			case 1:
			case 3:
			case 5:
			case 7:
			case 8:
			case 10:
			case 12:
				return findNext(d, m, y, 31);
			case 4:
			case 6:
			case 9:
			case 11:
				return findNext(d, m, y, 30);
			case 2:
				return findNext(d, m, y, ((y % 4 == 0 && y % 100 != 0) || (y % 400 == 0) ? 29 : 28));
			}
		}
		return "Invalid Date";
	}

}
```
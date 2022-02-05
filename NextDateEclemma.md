# Next Date Eclemma

```NextDateEclemma.java
package NextDate;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.Test;

class NextDateEclemma {
	
	NextDate n = new NextDate();
	
//	d == 1 and d < 1
	
	@Test
	void test1() {
		assertEquals(n.Next(1, 1, 1812), "2-1-1812");
	}
	
	@Test
	void test2() {
		assertEquals(n.Next(-1, 1, 1812), "Invalid Date");
	}
	
//	d == 31 and d > 31
	
	@Test
	void test3() {
		assertEquals(n.Next(32, 1, 1812), "Invalid Date");
	}
	
//	m == 1 and m < 1
	
	@Test
	void test4() {
		assertEquals(n.Next(1, -1, 1812), "Invalid Date");
	}
	
// m == 12 and m > 12
	
	@Test
	void test5() {
		assertEquals(n.Next(1, 13, 1812), "Invalid Date");
	}
	
// y == 1812 and y < 1812
	
	@Test
	void test6() {
		assertEquals(n.Next(5, 2, 1811), "Invalid Date");
	}

// y == 2022 and y > 2022
	
	@Test
	void test7() {
		assertEquals(n.Next(5, 4, 2023), "Invalid Date");
	}
	
// switch case coverage
	
	@Test
	void test8() {
		assertEquals(n.Next(5, 4, 2000), "6-4-2000");
	}
	
	@Test
	void test9() {
		assertEquals(n.Next(5, 2, 2000), "6-2-2000");
	}
	
	@Test
	void test10() {
		assertEquals(n.Next(5, 2, 2016), "6-2-2016");
	}
	
	@Test
	void test11() {
		assertEquals(n.Next(5, 2, 2015), "6-2-2015");
	}
	
// Boundary Values
	
	@Test
	void test12() {
		assertEquals(n.Next(31, 2, 2012), "Invalid Date");
	}
	
	@Test
	void test13() {
		assertEquals(n.Next(31, 1, 2012), "1-2-2012");
	}
	
	@Test
	void test14() {
		assertEquals(n.Next(31, 12, 2012), "1-1-2013");
	}
	
}

```
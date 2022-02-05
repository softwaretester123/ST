# Triangle Eclemma

```TriangleEclemma.java
package Triangle;

import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.Test;

class TriangleEclemma {

	Triangle t = new Triangle();

//  a,b,c = 1

	@Test
	void test1() {
		assertEquals(t.check(1, 1, 1), "Equilateral");
	}

//  a,b,c = 200
	@Test
	void test2() {
		assertEquals(t.check(200,200, 200), "Equilateral");
	}

//  a,b,c < 1

	@Test
	void test3() {
		assertEquals(t.check(0, 0, 0), "Invalid");
	}

	@Test
	void test4() {
		assertEquals(t.check(1, 0, 0), "Invalid");
	}

	@Test
	void test5() {
		assertEquals(t.check(1, 1, 0), "Invalid");
	}

//  a,b,c > 200
	@Test
	void test6() {
		assertEquals(t.check(201, 0, 0), "Invalid");
	}

	@Test
	void test7() {
		assertEquals(t.check(1, 201, 0), "Invalid");
	}

	@Test
	void test8() {
		assertEquals(t.check(1, 1, 201), "Invalid");
	}

//  a + b < c
	@Test
	void test9() {
		assertEquals(t.check(5, 7, 15), "Invalid");
	}

//  b + c < a
	@Test
	void test10() {
		assertEquals(t.check(15, 5, 7), "Invalid");
	}

//  c + a < b
	@Test
	void test11() {
		assertEquals(t.check(7, 15, 5), "Invalid");
	}

//  a != b and b != c
	@Test
	void test12() {
		assertEquals(t.check(7, 15, 15), "Isosceles");
	}

	@Test
	void test13() {
		assertEquals(t.check(7, 7, 5), "Isosceles");
	}

	@Test
	void test14() {
		assertEquals(t.check(7, 5, 7), "Isosceles");
	}

	@Test
	void test16() {
		assertEquals(t.check(7, 5, 6), "Scalene");
	}

}
```

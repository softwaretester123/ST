# Next Date BVA

```NextDateBVA.java

public class NextDate_Test {

// Normal BVA ( 5 out of 13 ) Variation in year ...(min min+ nom max- max)

@Test
public void test1() {
    assertEquals(NextDate.check(15, 6, 1812),"6-16-1812");
}
@Test
public void test2() {
    assertEquals(NextDate.check(15, 6, 1813),"16-6-1813");
}
@Test
public void test3() {
    assertEquals(NextDate.check(15, 6, 1912),"16-6-1912");
}
@Test
public void test4() {
    assertEquals(NextDate.check(15, 6, 2011),"16-6-2011");
}
@Test
public void test5() {
    assertEquals(NextDate.check(15, 6, 2012),"16-6-2012");
}

//Robust BVA ( 7 out of 19 ) Variation in Date ( min- min min+ nominal max- max max+) @Test

public void test6() {
    assertEquals(NextDate.check(6, 0, 1912),"Invalid Date");
}
@Test
public void test7() {
    assertEquals(NextDate.check(1, 6, 1912),"2-6-1912");
}
@Test
public void test8() {
    assertEquals(NextDate.check(2, 6, 1912),"3-6-1912");
}
@Test
public void test9() {
    assertEquals(NextDate.check(15, 6, 1912),"16-6-1912");
}
@Test
public void test10() {
    assertEquals(NextDate.check(30, 6, 1912),"1-7-1912");
}
@Test
public void test11() {
    assertEquals(NextDate.check(31, 6, 1912),"Invalid Date");
}
@Test
public void test12() {
    assertEquals(NextDate.check(32, 6, 1912),"Invalid Date");
}

// Worst Case BVA ( 5 out of 125 )

@Test
public void test13() {
    assertEquals(NextDate.check(15, 8, 1812),"16-8-1812");
}
@Test
public void test14() {
    assertEquals(NextDate.check(15, 8, 1813),"16-8-1813");
}
@Test
public void test15() {
    assertEquals(NextDate.check(15, 8, 1912),"16-8-1912");
}

@Test
public void test16()
{
    assertEquals(NextDate.check(15, 8, 2011),"16-8-2011");
}
@Test
public void test17() {
    assertEquals(NextDate.check(15, 8, 2012),"16-8-2012");
}

// worst Case robust bva ( 3 out of 343)

@Test
public void test18() {
    assertEquals(NextDate.check(44, 13, 2012),"Invalid Date");
}
@Test
public void test19() {
    assertEquals(NextDate.check(44, 1, 2021),"Invalid Date");
}
@Test
public void test20() {
    assertEquals(NextDate.check(4, 13, 2100),"Invalid Date");
}
}
```

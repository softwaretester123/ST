# Next Date BVA

```NextDateBVA.java

public class NextDate_Test {

// Normal BVA ( 5 out of 13 ) Variation in year ...(min min+ nom max- max)

@Test
public void test1() {
    assertEquals(NextDate.check(6, 15, 1812),"6/16/1812");
}
@Test
public void test2() {
    assertEquals(NextDate.check(6, 15, 1813),"6/16/1813");
}
@Test
public void test3() {
    assertEquals(NextDate.check(6, 15, 1912),"6/16/1912");
}
@Test
public void test4() {
    assertEquals(NextDate.check(6, 15, 2011),"6/16/2011");
}
@Test
public void test5() {
    assertEquals(NextDate.check(6, 15, 2012),"6/16/2012");
}

//Robust BVA ( 7 out of 19 ) Variation in Date ( min- min min+ nominal max- max max+) @Test

public void test6() {
    assertEquals(NextDate.check(6, 0, 1912),"Invalid Date");
}
@Test
public void test7() {
    assertEquals(NextDate.check(6, 1, 1912),"6/2/1912");
}
@Test
public void test8() {
    assertEquals(NextDate.check(6, 2, 1912),"6/3/1912");
}
@Test
public void test9() {
    assertEquals(NextDate.check(6, 15, 1912),"6/16/1912");
}
@Test
public void test10() {
    assertEquals(NextDate.check(6, 30, 1912),"7/1/1912");
}
@Test
public void test11() {
    assertEquals(NextDate.check(6, 31, 1912),"Invalid Date");
}
@Test
public void test12() {
    assertEquals(NextDate.check(6, 32, 1912),"Invalid Date");
}

// Worst Case BVA ( 5 out of 125 )

@Test
public void test13() {
    assertEquals(NextDate.check(8, 15, 1812),"8/16/1812");
}
@Test
public void test14() {
    assertEquals(NextDate.check(8, 15, 1813),"8/16/1813");
}
@Test
public void test15() {
    assertEquals(NextDate.check(8, 15, 1912),"8/16/1912");
}

@Test
public void test16()
{
    assertEquals(NextDate.check(8, 15, 2011),"8/16/2011");
}
@Test
public void test17() {
    assertEquals(NextDate.check(8, 15, 2012),"8/16/2012");
}

// worst Case robust bva ( 3 out of 343)

@Test
public void test18() {
    assertEquals(NextDate.check(13, 44, 2012),"Invalid Date");
}
@Test
public void test19() {
    assertEquals(NextDate.check(1, 44, 2021),"Invalid Date");
}
@Test
public void test20() {
    assertEquals(NextDate.check(13, 4, 2100),"Invalid Date");
}
}
```

# Next Date Equivalence

```NextDateEquivalence.java

// Strong Normal and Weak Normal @Test

public void test21() {
    assertEquals(NextDate.check(2, 15, 2010),"2/16/2010");
}

@Test
public void test22() {
    assertEquals(NextDate.check(4, 6, 2008),"4/7/2008");
}

@Test
public void test23() {
    assertEquals(NextDate.check(2, 15, 2011),"2/16/2011");
}

// Weak Robust

@Test
public void test24() {
    assertEquals(NextDate.check(-1, 15, 2011),"Invalid Date");
}

@Test
public void test25() {
    assertEquals(NextDate.check(2, 56, 2011),"Invalid Date");
}

@Test
public void test26() {
    assertEquals(NextDate.check(3, 15, 2045),"Invalid Date");
}

//Strong Robust

@Test
public void test27() {
    assertEquals(NextDate.check(-1, 40, 2004),"Invalid Date");
}

@Test
public void test28() {
    assertEquals(NextDate.check(7, 67, 2045),"Invalid Date");
}

@Test
public void test29() {
    assertEquals(NextDate.check(-1, 16, 2045),"Invalid Date");
}
```
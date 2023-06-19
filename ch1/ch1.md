1.1.1 아래 각 표현식의 결괏값은 무엇인가?
 a. (0+15) /2  
 // 7.5
 b.2.0e-6*100000000.1
 // 200.0000002
 c.true && false || true && true
 // true

 2. 각 표현식의 결과 데이터 타입은 무엇인가 
 a (1+2.236)/2  //double
 b 1+2+3+4.0 // double 
 c 4.1 >= 4 // boolean
 d 1+2+"3" // string

 3. 명령어를 인수로 3개의 정수를 받고 그 값들이 모두 같으면 "equal" 다르면 "not equal" 문자를 작성하는 프로그램을 작성하라. 
 
 ```
 public class CompareIntegers {
    public static void main(String[] args) {
        if (args.length != 3) {
            System.out.println("잘못된 인수입니다. 세 개의 정수를 입력해주세요.");
            return;
        }

        int num1 = Integer.parseInt(args[0]);
        int num2 = Integer.parseInt(args[1]);
        int num3 = Integer.parseInt(args[2]);

        if (num1 == num2 && num2 == num3) {
            System.out.println("equal");
        } else {
            System.out.println("not equal");
        }
    }
}

const CompareIntegers = (num1, num2, num3) => {

  if (Number.isInteger(a)) {
      console.log("not equal");
  }
  if (Number.isInteger(b)) {
      console.log("not equal");
  }
  if (Number.isInteger(c)) {
      console.log("not equal");
  }

  if (num1 === num2 && num2 === num3) {
    console.log("equal");
  } else {
    console.log("not equal");
  }
}


const args = process.argv.slice(2);

if (args.length !== 3) {
  console.log("잘못된 인수입니다. 세 개의 정수를 입력해주세요.");
} else {

  if (Number.isInteger(num1)) {
      console.log("not equal");
  }
  if (Number.isInteger(num2)) {
      console.log("not equal");
  }
  if (Number.isInteger(num3)) {
      console.log("not equal");
  }

  if (num1 === num2 && num2 === num3) {
    console.log("equal");
  } else {
    console.log("not equal");
  }

}

```

4. 아래 각 구문에서 틀린부분을 찾아보아라 
 각 구문에서 틀린부분이 있다면 찾아보아라 
a. if(a>b) then c=0;
// then 키워드 필요없음 
b.if a>b {c=0;}
// 소괄호 없음 
```
if(a > b) {
    c = 0;
}
```
c. if(a>b) c = 0;
틀린건 없지만 사실 중괄호를 쓰는걸 권장하는편.. 

d. if(a>b) c = 0 else b = 0 

틀린건 없지만 사실 중괄호를 쓰는걸 권장하는편.. 

5. double 타입 변수 x,y가 정확히 0과 1사이에 있으면 true를 출력하고 그렇지않으면 false를 출력하는 프로그램을 작성하라. 


 ```
 public class CheckRange {
    public static void main(String[] args) {
         if (args.length != 2) {
            System.out.println("잘못된 인수입니다. 두 개의 소스를");
            return;
        }

        boolean isInRange = (x > 0 && x < 1) && (y > 0 && y < 1);

        System.out.println(isInRange);
    }
}
```

return  (x > 0 && x < 1) && (y > 0 && y < 1)



6. 아래의 코드는 어떤값을 출력하는가?
```
int f = 0; int g = 1; 
for (int i =0; i<=15; i++>) {
    stdOut.println(f);
    f = f+g; 
    g = f-g;
}

```
0 // f = 0+1, g = 1-1
1 // f = 1+0, g = 1-0
1 // f = 1+1, g = 2-1
2 // f = 2+1, g = 3-1
3
5
8
13
21
34
55
89
144
233
377
610
```

7, 아래의 각 코드가 어떤 값을 출력하는지 구하라. 
a.
```
double t = 9.0 
while (Math.abs(t-9.0/t)>.001)
    t = (9.0/t + t) /2.0
StdOut.printf("%.5f\n",t)
```
// 3.00009 

b. 
```
int sum = 0; 
for (int i = 1; i<1000; i++) 
    for (int j = 0; j<i ; j++) 
        sum++
    StdoutPrintln(sum)
```
// 499500
c
```
int sum = 0; 
for (int i = 1; i<1000; i*=2) 
    for (int j = 0; j<1000; j++)
        sum++
    StdoutPrintln(sum)
```
// 10000

8. 아래의 각 코드가 출력하는 값을 구하고 그 이유를 설명하라. 
a. Ssytem.out.println('b') // b
b. System.out.println('b'+'c') //bc
c. System.out.println((char)('a'+4)) // e

9. 양의 정수 N을 이진수로 표현한 String타입 변수 s로 변환하는 코드를 작성하라. 
```
int N = 42; // 변환할 양의 정수
StringBuilder sb = new StringBuilder();

while (N > 0) {
    sb.insert(0, N % 2);
    N = N / 2;
}

String s = sb.toString();

```

```
**숫자를 이진수로 변환**
주어진 숫자를 2로 나누기
나머지를 구하기 -> 나머지는 0 또는 1
나머지를 오른쪽에서부터 순서대로 출력
몫을 으로 다시 처음부터 
몫이 0이 될 때까지 위의 과정을 반복
```

10. 아래 코드의 잘못된 점을 찾으라. 
int[] a; 
for (int i = 0; i<10; i++) 
    a[i] = i*i 

// a 초기화 안함. 메모리 할당필요. 

11. boolean 타입 2차원 배열의 항목들을 출력하는 코드를 작성하라. 
항목의 값이 true이면 *를 출력하고 false이면 공백을 출력한다. 이때 행과 열의 번호도 출력한다. 
```
boolean[][] array = {
    {true, false, true},
    {false, true, false},
    {true, true, false}
};

for (int i = 0; i < array.length; i++) {
    for (int j = 0; j < array[i].length; j++) {
        System.out.print("[" + i + "," + j + "] ");

        if (array[i][j]) {
            System.out.print("*");
        } else {
            System.out.print(" ");
        }
    }
    System.out.println();
}
```

const checkFloat = (x, y) => x%1 === 0 && y%1 ===0 

x%1 === 0 && y%1 ===0 

12. 아래 코드는 어떤 값을 출력하는가?
```
int[] a = new int[10];
for (int i = 0; i<10; i++) 
    a[i] = 9-i // 9, 8, 7, 6, 5, 4, 3, 2, 1, 0
for (int i = 0; i<10; i++) 
    a[i] = a[a[i]] // 9, 8, 7, 6, 5, 4, 3, 2, 1, 0
for (int i = 0; i<10; i++) 
    System.out.println(a[i]) // 9, 8, 7, 6, 5, 4, 3, 2, 1, 0
```

13. 2차원 배열의 행과 열을 바꾸는 (90도 회전)코드를 작성하라. 즉 원본이 N열 M행이었다면 바뀐 행열은 M열 N행이어야한다. 
```
int[][] originalArray = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

int originalRows = originalArray.length;
int originalCols = originalArray[0].length;

int[][] transposedArray = new int[originalCols][originalRows];

for (int i = 0; i < originalRows; i++) {
    for (int j = 0; j < originalCols; j++) {
        transposedArray[j][i] = originalArray[i][j];
    }
}
```

14. int값 N을 인수로 받아서 log2N이하의 가장 큰 정수를 리턴하는 static 메서드 lg()를 구현하라. 단 자바에서 제공되는 편의 클래스 Math를 이용하지말고 직접 구현하라. 

15. int배열 변수 a[]와 int값 M을 인수로 받는 static메서드 histogram()을 작성하라. 이 메서드는 크기 Mdml int배열을 리턴해야하는데 그 배열의 i번째 항목은 인수로 받은 a[]의 각 항목들의 값이 모두 0과 m-1사이에 있다면 리턴되는 배열의 항목들의 총합이 a.length와 같아야한다. 


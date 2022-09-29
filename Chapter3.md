# 3. 빅 오 표기법
**연습문제**

모두 BigO 클래스의 메소드입니다.


- 1 .  윤년 판단 : O(1)
~~~Java
public boolean isLeapYear(int year)
{
    return (year%100 == 0) ? (year%400 == 0) : (year%4 ==0);
}
~~~

- 2 . 배열 합 : O(N)
~~~Java
public int arraySum(int array[])
{
    int sum = 0;
    for (int i=0; i<array.length; i++>)
    {
        sum += array[i];
    }
    return sum;
}
~~~

- 3 . 복리(체스판과 쌀) : O(logN)
~~~Java
	public int chessboardSpace(int numOfGrains)
	{
		int chessboardSpaces = 1;
		int placedGrains = 1;
		
		while(placedGrains < numOfGrains)
		{
			placedGrains *= 2;
			chessboardSpaces += 1;
		}
		return chessboardSpaces;
	}
	
~~~

- 4 . "a"로 시작하는 문자열 포함한 새 배열 반환 : O(N)
~~~Java
import java.util.*;

public String[] selectAStrings(String[] array)
	{
		ArrayList<String> a = new ArrayList<String>();
		for (int i=0; i<array.length; i++)
		{
			if (array[i].charAt(0) == 'a')
			{
				a.add(array[i]);
			}
		}
		String[] newArr = new String[a.size()];
		for (int i=0; i<newArr.length; i++)
		{
			newArr[i] = a.get(i);
		}
		return newArr;
		
	}
~~~
출력 예시  (출력값 : [abc, asd])
~~~Java
import java.util.*;

	public static void main(String[] args) {
		String str[] = {"abc", "dfg", "asd"};
		String newStr[] = new BigO().selectAStrings(str);
		System.out.println(Arrays.toString(newStr));
	}
~~~

- 5 . 정렬된 배열의 중앙값 : O(1)
~~~Java
	public double median(int array[])
	{
		int middle = array.length/2;
		
		if (array.length%2 == 0)
		{
			return (array[middle - 1] + array[middle])/2.0;
		}
		else
		{
			return array[middle];
		}
	}
~~~
출력 예시  (출력값 : 2.5)
~~~Java
public static void main(String[] args) {
		int arr[] = {1,2,3,4};
		double med = new BigO().median(arr);
		System.out.println(med);
	}
~~~
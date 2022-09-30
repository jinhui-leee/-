# 빅 오로 코드 속도 올리기
## 버블 정렬 : O(N^2)
~~~Java
public int[] bubbleSort(int[] array)
	{
		int unsortedUntilIndex = array.length - 1;
		boolean sorted = false;
		
		while (sorted != true)
		{
			sorted = true;
			
			for (int i=0; i<unsortedUntilIndex; i++)
			{
				if (array[i] > array[i+1])
				{
					int tmp = array[i];
					array[i] = array[i+1];
					array[i+1] = tmp;
					sorted = false;
				}
			}
			unsortedUntilIndex -= 1; 
		}
		return array;
	}
~~~
출력 예시 : [2, 4, 5, 7, 9]
~~~Java
public static void main(String[] args) {
		int arr[] = {7,2,5,4,9};
		BigO b = new BigO();
		b.bubbleSort(arr);
		System.out.println(Arrays.toString(b.bubbleSort(arr)));
	}
~~~

# 이차 문제와 선형 해결법
-  배열 중복 숫자 확인 : O(N^2)

 ~~~Java
public boolean hasDuplicateValue(int[] array)
 {
     for (int i=0; i<array.length; i++)
     {
         for (int j=0; j<array.length> j++)
         {
             if (i != j && array[i] == array[j])
             {
                return true;
            }
         }
    }
     return false;
 }
~~~
- 배열 중복 숫자 확인 : O(N)
~~~Java
import java.util.*;

     public boolean hasDuplicateValueN(int[] array)
	 {
    	HashMap<Integer, Integer> hashMap = new HashMap<Integer, Integer>();
    	
    	for (int i=0; i<array.length; i++)
    	{
    		if (hashMap.containsKey(array[i]) == true)
    		{
    			return true;
    		}
    		else
    		{
    			hashMap.put(array[i], 0);
    		}
    	}	
    	return false;
    }
 
 ~~~


# 연습 문제
3. 배열 모든 숫자 쌍의 최대곱 찾기 : O(N^2)

~~~Java
public int greatestProduct(int[] array)
{	
	int greatestProductSoFar = array[0]*array[1];

	for (int i=0; i<array.length; i++)
	{
		for (int j=0; j<array.length; j++)
		{
			if (i != j && array[i]*array[j] > greatestProductSoFar)
			{
				greatestProductSoFar = array[i]*array[j];
			}
		}
	} 
	return greatestProductSoFar;
}
~~~

4. 배열에서 가장 큰 수 찾기 : O(N)

~~~Java
public int greatestNumer(int[] array)
{
	int maxNum = array[0];

	for (int i=1; i<array.length; i++)
	{
		if (maxNum < array[i])
		{
			maxNum = array[i];
		}
	}
	return maxNum;
}
~~~
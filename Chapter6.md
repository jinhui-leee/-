# 긍정적인 시나리오 최적화
- 삽입 정렬 : O(N^2)

~~~Java
	public int[] insertionSort(int array[]) 
	{
		for (int i=0; i<array.length; i++)
		{
			int tmpValue = array[i];
			int position = i - 1;
			
			while(position >= 0)
			{
				if (array[position] > tmpValue)
				{
					array[position+1] = array[position];
					position = position - 1;
				}
				else
				{
					break;
				}
			}
			array[position+1] = tmpValue;
		}
		return array;
	}
~~~

- 예제  
두 배열의 교집합 배열 반환 : O(N^2)
~~~Java 
import java.util.*;
 
 public int[] intersection(int[] firstArr, int[] secondArr)
    {
    	Vector<Integer> intersectionV = new Vector<Integer>();
    	
    	for (int i=0; i<firstArr.length; i++)
    	{
    		for (int j=0; j<secondArr.length; j++)
    		{
    			if (firstArr[i] == secondArr[j])
    			{
    				intersectionV.add(firstArr[i]);
    				break;
    			}
    		}
    	}
    	
    	int result[] = new int[intersectionV.size()];
    	for (int i=0; i<result.length; i++)
    	{
    		result[i] = intersectionV.get(i);
    	}
    	return result;
    }
~~~

# 연습문제
3.1 배열에서 합하면 10이 되는 숫자 쌍 판단
- 최선의 시나리오 : array[0]과 array[1]의 합이 10일 경우
- 최악의 시나리오 : 10이 되는 숫자 쌍이 없는 경우
~~~Java
  public boolean twoSum(int[] array)
    {
    	for(int i=0; i<array.length; i++)
    	{
    		for (int j=0; j<array.length; j++)
    		{
    			if ((i != j) && (array[i] + array[j] == 10))
    			{
    				return true;
    			}
    		}
    	}
    	return false;
    }

~~~

3.2 "X"가 문자열에 있는지 판단 : O(N)
~~~Java
 public boolean containsX(String str)
    {	
    	for (int i=0; i<str.length(); i++)
    	{
    		if (str.charAt(i) == 'X')
    		{
    			return true;
    		}
    	}
    	return false;
    }
~~~
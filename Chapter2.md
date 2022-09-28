# 2. 알고리즘이 중요한 까닭

- 선형 검색 Linear search
~~~Java
public class Search<T> {
	public Object linearSearch(Object[] array, T searchValue)
	{
		for (int i=0; i<array.length; i++)
		{
			if (array[i] == searchValue)
			{
				return i; 
			}
            if (array[i] < searchValue)
            {
                return null
            }
		}
		return null;
	}
}
~~~

- 정렬된 배열 선형 검색(int형)
~~~Java
public class Search {
	public Object linearSearch(int[] array, int searchValue)
	{
		for (int i=0; i<array.length; i++)
		{
			if (array[i] == searchValue)
			{
				return i; 
			}
			if (array[i] > searchValue)
			{
				return null;
			}
		}
		return null;
	}
}

~~~

- 이진검색 Binary Search
~~~Java
public class Search {
	public Object binarySearch(int array[], int value)
	{
		
		int lowerBound = 0;
		int upperBound = array.length-1;
		
		while(lowerBound <= upperBound)
		{
			int midPoint = (upperBound + lowerBound)/2;
			int valueAtMidPoint = array[midPoint];
			
			if (value == valueAtMidPoint)
			{
				return midPoint;
			}
			else if (value < valueAtMidPoint)
			{
				upperBound = midPoint - 1;
			}
			else if (value > valueAtMidPoint)
			{
				lowerBound = midPoint + 1;
			}
		}
		return null;
	}
}

~~~

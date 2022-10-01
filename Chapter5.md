# 빅 오를 사용하거나 사용하지 않는 코드 최적화
- 선택 정렬 : O(N^2)
~~~Java
public int[] secletionSort(int[] array)
{
    for (int i=0; i<array.length-1; i++)
    {
        int lowestNumIndex = i;

        for (int j = i+1; j<array.length; j++)
        {
            if (array[j] < array[lowestNumIndex])
            {
                lowestNumIndex = j;
            }
        }

        if (lowestNumIndex != i)
        {
            int tmp = array[i];
            array[i] = array[lowestNumIndex];
            array[lowestNumIndex] = tmp;
        }
    }
    return array;
}
~~~

# 연습 문제

3. 배열의 모든 수를 2배로 만든 새 배열 합 반환 : O(N)
~~~Java
   public int doubleThenSum(int[] array)
    {
    	int newArray[] = new int[array.length];
    	int sum = 0;
    	for(int i=0; i<array.length; i++)
    	{
    		newArray[i] = array[i]*2;
    		sum += newArray[i];
    	}
    	return sum;
    }
~~~

4. 문자열 배열의 다양한 출력 : O(N)
~~~Java
    public void multipleCases(String[] array)
    {
    	for (int i=0; i<array.length; i++)
    	{
    		System.out.println(array[i].toUpperCase());
    		System.out.println(array[i].toLowerCase());
    		System.out.println(array[i].substring(0,1).toUpperCase() + array[i].substring(1));
    	}
    }

~~~

5. 인덱스가 짝수이면 배열 내 모든 수에 그 인덱스 값을 더해 출력 : O(N^2)
~~~Java
  public void everyOther(int[] array)
    {
    	for(int i=0; i<array.length; i++)
    	{
    		if (array[i]%2 == 0)
    		{
    			for (int j=0; j<array.length; j++)
    			{
    				System.out.println(array[j] + array[i]);
    			}
    		}
    	}
    }
~~~

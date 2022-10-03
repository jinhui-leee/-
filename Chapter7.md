# 일상적인 코드 속 빅 오
- 짝수의 평균
~~~Java
 public double avrOfEvenNumers(int[] array)
    {
    	double sum = 0.0;
    	int evenNumCnt = 0;
    	
    	for (int i=0; i<array.length; i++)
    	{
    		if (array[i]%2 == 0)
    		{
    			sum += array[i];
    			evenNumCnt += 1;
    		}
    	}
    	return sum/evenNumCnt;
    }
~~~

- 단어 생성기
~~~Java
 public String[] wordBuilder(char[] array)
    {
    	ArrayList<String> newArr = new ArrayList<String>();
    	
    	for (int i=0; i<array.length; i++)
    	{
    		for (int j=0; j<array.length; j++)
    		{
    			if (i != j)
    			{
    				newArr.add(Character.toString(array[i]) + Character.toString(array[j]));
    			}
    		}
    	}
    	
    	String collection[] = new String[newArr.size()];
    	
    	for (int i=0; i<newArr.size(); i++)
    	{
    		collection[i] = newArr.get(i);
    	}
    	return collection;
    }
~~~

- 배열 예제
~~~Java
  public int[] sample(int[] array)
    {

    	int first = array[0];
    	int middle = array[array.length/2];
    	int last = array[array.length-1];
    	
    	int newSample[] = {first, middle, last};
    	
    	return newSample;
    }
~~~

- 평균 섭씨 온도 구하기
~~~Java

~~~

- 의류 상표
~~~Java

~~~

- 1 세기
~~~Java

~~~

- 팬린드롬 검사기
~~~Java

~~~

- 모든 곱 구하기
~~~Java

~~~

- 암호 크래커
~~~Java

~~~

# 연습 문제
1. 합이 100이 되는 배열 판단 : O(N)
~~~Java

~~~

2. 정렬된 두 배열을 병합한 새 정렬 배열 생성 : O(N)
~~~Java

~~~

3. 문자열 찾기(바늘 찾기) : O(N+M)
~~~Java

~~~

4. 배열의 세 수를 곱해 가장 큰 값 찾기 : O(N^3)
~~~Java

~~~

5. 랜덤으로 이력서 뽑기 : O(log N)
~~~Java

~~~
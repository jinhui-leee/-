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
public double avrC(double[] fReadings)
    {
    	double c[] = new double [fReadings.length]; 
    	double sum = 0;
    	for (int i=0; i<fReadings.length; i++)
    	{
    		c[i] = (fReadings[i] - 32)/1.8; 
    		sum += c[i];
    	}
    	return sum/c.length;
    	
    }
~~~

- 의류 상표
~~~Java
public String[] markInventory(String []clothingItems)
    {
    	String clothingOptions[] = new String[clothingItems.length*5];
    	int n = 0;
    	
    	for (int i=0; i<clothingItems.length; i++)
    	{
    		for (int j=1; j<=5; j++)
    		{
    			clothingOptions[n] = clothingItems[i] + " Size: " + Integer.toString(j);
    			n += 1;
    		}
    	}
    	return clothingOptions;
    }
~~~

- 1 세기
~~~Java
public int countOnes(int[][] outerArr)
    {
    	int cnt = 0;
    	for (int i=0; i<outerArr.length; i++)
    	{
    		for (int j=0; j<outerArr[i].length; j++)
    		{
    			if (outerArr[i][j] == 1)
    			{
    				cnt += 1;
    			}
    		}
    	}
    	return cnt;
    }
~~~

- 팬린드롬 검사기
~~~Java
public boolean isPalindrome(String str)
    {
    	int leftIndex = 0;
    	int rightIndex = str.length()-1;
    	
    	while (leftIndex < rightIndex)
    	{
    		if (str.charAt(leftIndex) != str.charAt(rightIndex))
    		{
    			return false;
    		}
    		leftIndex++;
    		rightIndex--;
    	}
    	return true;
    }
~~~

- 모든 곱 구하기
~~~Java
 public int[] twoNumberProducts(int[] arr)
    {
    	int[] products = new int[arr.length*(arr.length-1)/2];
    	int n = 0;
    	for (int i=0; i<arr.length-1; i++)
    	{
    		for (int j=i+1; j<arr.length; j++)
    		{
    			products[n] = arr[i]*arr[j];
    			n++;
    		}
    	}
    	return products;
    }
~~~

- 암호 크래커
~~~Java

~~~

# 연습 문제
1. 합이 100이 되는 배열 판단 : O(N)
~~~Java
public boolean oneHundredSum(int[] arr)
    {
    	int leftIndex = 0;
    	int rightIndex = arr.length-1;
    	
    	while(leftIndex < rightIndex)
    	{
    		if (arr[leftIndex] + arr[rightIndex] != 100)
    		{
    			return false;
    		}

    		leftIndex++;
    		rightIndex--;

    	}
    	return true;
    }
~~~

2. 정렬된 두 배열을 병합한 새 정렬 배열 생성 : O(N)
~~~Java
public int[] merge(int[] arr1, int[] arr2)
    {
    	int pointer1 = 0;
    	int pointer2 = 0;
    	
    	int[] newArr = new int[arr1.length+arr2.length];
    	
    	for (int i=0; i<newArr.length; i++)
    	{
    		if (pointer1 == arr1.length)
    		{
    			newArr[i] = arr2[pointer2];
    			pointer2++;
    		}
    		else if (pointer2 == arr2.length)
    		{
    			newArr[i] = arr1[pointer1];
    			pointer1++;
    		}
    		else
    		{
    			if (arr1[pointer1] > arr2[pointer2])
        		{
        			newArr[i] = arr2[pointer2];
        			pointer2++;
        		}
        		else
        		{
        			newArr[i] = arr1[pointer1];
        			pointer1++;
        		}
    		}
    	}
    	return newArr;
    }
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
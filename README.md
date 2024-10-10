# SWE_2021_41_2024_2_week_6
---
## WeeK 4 Assignment
* Link of your repository    [Github](https://github.com/Lee-seunghyeon2/-SWE_2021_41_2024_2_week_4/blob/main/2021310999_%EC%9D%B4%EC%8A%B9%ED%98%84%20(5).ipynb)  
</pre>

```python
def isHappy(n):

    thisset = set()

    while n not in thisset:
        thisset.add(n)
        number = []
        while n != 0:
            temp = n % 10
            number.append(temp*temp)
            n //= 10

        if sum(number) == 1:
            return True
        else:
            n = sum(number)

    return False

    return

print(isHappy(int(input())))
```
* Description of your code
> ishappy()는 입력받은 숫자가 happy num인지 확인하는 함수이다. 이때 happy num은 각 자리수의 제곱의 합을 구하고, 다시 그 합을 입력받는 수로 사용하여, 합이 1이 나올 수 있는 수이다.
> 예를 들어 19를 입력받게 되면 1과 9의 제곱의 합인 82가 다음 입력값으로 들어가게 되며, 그 다음에는 8과 2의 제곱의 합인 68이, 그 다음에는 100 마지막으로는 1이 결과값으로 나오게 되어 19는 happy num이다.
> 하지만 입력값이 1이 나오지 않고 이전에 나왔던 수와 똑같은 수가 나오게 된다면, 그 수는 happy num이 아니다.
>
> 이를 실행시키기 위하여 단계를 나누면
> 1. 각 자리의 제곱의 합을 구하기.
> 2. set()은 중복을 허용하지 않으니 입력값이 1이 아니라면 set에 추가, 1이라면 True를, set안에 있는 수가 입력값이면 False를 반환하기.
> 3. 위의 과정을 결과값이 나올 때 까지 반복하기
>
> 이렇게 총 3 단계로 나눠지게 된다.
> 1번의 과정은 list를 만들어 각 자리를 제곱의 값을 list에 추가하였고, sum을 이용하여 list의 합을 구하였다.
> 2번의 과정은 set을 만들어 list의 합이 1이라면 True를 반환하도록, 그렇지 않으면 set에 추가되도록 하였다.
> 3번의 과정은 while 반복문을 
---
## Week 5 Assignment


</pre>

>```python  
>docker exec ubuntu-container cat /etc/os-release 
>``` 
>* Explanation of commaindline and your ouptut
>* output:
>> PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
>>LOGO=ubuntu-logo
>* Explanation: 실행중인 docker container에서 cat 명령어를 사용하여 /etc/os-release 내용을 출력한다.
이때 container의 이름은 ubuntu-container이다.

</pre>  

>```python   
>docker exec ubuntu-container git --version
>```
>* Explanation of commaindline and your ouptut
>* output: git version 2.43.0
>* Explanation: 실행중인 docker container에서 git의 설치 여부와 버젼 정보를 출력한다.
이때 container의 이름은 ubuntu-container이다.

</pre>

>```python   
>docker exec ubuntu-container python3 --version
>```
>* Explanation of commaindline and your ouptut
>* output: Python 3.12.3
>* Explanation: 실행중인 docker container에서 python의 설치 여부와 버젼 정보를 출력한다.
이때 container의 이름은 ubuntu-container이다.

</pre>

>```python   
>docker inspect --format="{{ .HostConfig.Binds }}" ubuntu-container
>```
>* Explanation of commaindline and your ouptut
>* output: [./ossp_host_dir:/mnt/ubuntu-container_dir]
>* Explanation: docker inspect을 통하여 docker container의 정보를 확인한다.
이때 확인할 정보는 .HostConfig.Binds이며 container 이름은 ubuntu-container이다.
결과로 host 디렉토리와 container 디렉토리에서 마운트된 디렉토리를 보여준다.
